# PEPP-PT FAQ

## Why does the German PEPP-PT implementation use push notifications?

Firebase Cloud Messaging (FCM) and Apple Push Notification service (APNs) are
not the only way to send data from a backend to the device.  However, they are
the only transport mechanisms that are integrated in the mobile operating
systems and allow receiving messages in the background and during standby.

The German PEPP-PT implementation does not require any specific messaging
service.  But for a large-scale deployment and an acceptable user experience,
FCM and APNs can be good ways to go.

Note the push message provider does not learn anything about the user.  The
message payload is a mere random number, and the design includes "noise"
messages to disguise "real" messages to at-risk users in order to avoid that
the provider can learn anything from traffic analysis.

The German PEPP-PT implementation and also ROBERT do not necessarily require
FCM and APNs.  An implementer who wishes to avoid push services could use
a pull-based solution, which is technically feasible, but it requires
significant compromises on scalability, usability, energy consumption, and time
to notification.

Also note that push services are provided by manufacturers of the operating
system, so there is no need to trust an additional party.

## Isn't it a problem that central servers could be attacked with DDoS?

Any central service is at risk of being taken down by DDoS.

All proximity tracing solutions rely on a central backend to deliver messages
to the phones (PEPP-PT, as well as DP-3T, Covid-Watch, the Google and Apple
proposals, etc).

Hosting providers of such backend services must always take DDoS protection
measures, just as any other high-availability service.

PEPP-PT does not dictate how the hosting of the backend servers should be done.
