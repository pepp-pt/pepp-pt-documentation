# PEPP-PT FAQ

## Who is PEPP-PT?

An overview of most of our partners can be found on our website. However, as we
have recently onboarded new partners and are right now in the process of
rebuilding our website, not all of our partners can be found there yet. A major
focus of our new website, however, will be to provide more transparency on our
partners as well as our governance structure. Please bear with us as we update
this information.

## Does PEPP-PT accept technical input from the public?

Our first and foremost goal is to provide a technology that will enable the
development of coronavirus contact tracing apps that are 100 percent compliant
with the European GDPR and interoperable across borders. In order to do so,
PEPP-PT was set up as a multinational initiative bringing together experts from
various different fields and from across Europe.

Therefore, we explicitly welcome and input from anyone who would like to
participate in this project and work towards our goal. There are various ways
by which we facilitate this – one being the [PEPP-PT discussion
group](https://groups.google.com/forum/#!forum/pepp-pt-discussion).  A more
formal way to engage with us and contribute to our work would be to become
a partner.

## What is the plan with the open-source releases?

We have always said that we will make the code available to the public as open
source, and we will do so.  We decided, however, that before publishing
a repository, it must be complete and have undergone quality and security
testing.

At this time, the following code is available in the [PEPP-PT GitHub
organization](https://github.com/pepp-pt):

* [Android application core library](https://github.com/pepp-pt/pepp-pt-ntk-core-android)
* [Android application reference implementation](https://github.com/pepp-pt/pepp-pt-ntk-sample-android)

We will continue releasing further repositories as they become available.

## What is the PEPP-PT position on centralized vs decentralized?

At PEPP-PT, we are committed to two principles: First, the privacy of users and
data protection must be guaranteed at all times. Secondly, there must be enough
flexibility to tailor the technology to the respective requirements of
individual countries – while maintaining its interoperability.

We believe that this flexibility also applies to contact tracing in the event of
a positive coronavirus test. For this case, there are two approaches – a
centralized and a decentralized approach. PEPP-PT is open to both, and will thus
offer both models in the future.

However, the rapid fight against the pandemic has first priority. This is why we
want to provide an effective technology as quickly as possible. As of today, the
development of the low-data approach has progressed considerably – especially
with regard to the interoperability of the technology. Since the pandemic is not
a national phenomenon, we consider this point to be of particular importance.

At the same time, the centralized approach is an important element in managing
the pandemic, as statistical data on the spread and effectiveness of the
measures is thus available more quickly. As of today, we consider this approach
to be more effective.

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

## Won't using a single secret key allow bad actors to eventually de-anonymize users?

PEPP-PT avoids this problem by never revealing the long-term keys but rather by
matching EBIDs to PUIDs in the backend, running the risk assessment and only
then notifying the users which are determined to be at risk of an infection.

An attacker will be "at risk" herself, i.e. for more than a few minutes at a
close distance to an infected person.  By definition, this makes it not an
attack, but a viable notification of being "at risk".

An attacker will not be able to de-anonymize the infected person just from the
notification.  There are scenarios where a user might learn who has possibly
infected whom: imagine having just a single close contact over 21 days and then
receiving a notification.  But from the protocol itself, it is not possible, as
opposed to a design where keys are broadcast.

## How can I get PEPP-PT to certify my contact tracing app?

App developers must first receive the backing of the respective government.
After receiving the official backing of the government and finalizing an
application, we will review the code and technical specifications.
