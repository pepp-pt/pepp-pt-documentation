# PEPP-PT Documentation

## What is PEPP-PT?

The purpose of the Pan-European Privacy-Preserving Proximity Tracing (PEPP-PT)
approach is to provide a common basis for management systems that can be
integrated into national public health responses to the COVID-19 pandemic.  The
PEPP-PT approach is being created by a multi-national European team.  It is
a privacy-preserving digital proximity-tracing approach, which is in full
compliance with GDPR and can also be used when traveling between countries.

## Documentation

Main documents:

- [PEPP-PT High-Level Overview](./PEPP-PT-high-level-overview.pdf)
- [PEPP-PT Building Blocks for Pandemic Management Systems using Proximity Tracing](./PEPP-PT-building-blocks.pdf)
- [PEPP-PT Data Protection and Information Security Architecture: Illustrated on German Implementation](./10-data-protection/PEPP-PT-data-protection-information-security-architecture-Germany.pdf)

The building blocks will be published as separate documents step by step as we
complete the editing process.

![building blocks](./img/blocks.png)

### Smartphone app

Folder [01-smartphone-app](./01-smartphone-app)

```
01-smartphone-app/PEPP-PT-sample-app.pdf
```

### Infection status verification service

Folder [02-infection-verification](./02-infection-verification)

### Proximity warning service

Folder [03-proximity-warning](./03-proximity-warning)

```
03-proximity-warning/PEPP-PT-overview-proximity-warning.pdf
```

### National health policy framework

Folder [04-health-policy](./04-health-policy)

### Pandemic management planning framework

Folder [05-pandemic-framework](./05-pandemic-framework)

### Epidemiological validation frameworks

Folder [06-epidemiological-validation](./06-epidemiological-validation)

### Operational pandemic management backbone

Folder [07-operational-backbone](./07-operational-backbone)

### Planning pandemic management backbone

Folder [08-planning-backbone](./08-planning-backbone)

### Inter-country federation service

Folder [09-federation](./09-federation)

### Data protection protocol

Folder [10-data-protection](./10-data-protection)

```
10-data-protection/PEPP-PT-data-protection-information-security-architecture-Germany.pdf
10-data-protection/ROBERT-concept-illustration.pdf
10-data-protection/ROBERT-specification-EN-v1_0.pdf
```

The primary location of the ROBERT approach is
<https://github.com/ROBERT-proximity-tracing/documents>.  Please use the
primary location for comments and discussions about ROBERT.

### Secure communication protocol

Folder [11-secure-communication](./11-secure-communication)

### Proximity measurement

Folder [12-proximity-measurement](./12-proximity-measurement):

```
12-proximity-measurement/2020-04-01-BW-report-epi-mod.pdf
12-proximity-measurement/2020-04-07-BW-report-epi-mod.pdf
12-proximity-measurement/2020-04-09-BW-report-epi-mod.pdf
12-proximity-measurement/distance-measurements-and-classification-20200406.pdf
```

## FAQ

See [FAQ](./FAQ.md).

## Open source strategy

PEPP-PT is preparing a number of source code repositories to be open sourced.

These repositories include:

* Backend services
* Android application core libraries
* Android application reference implementation
* iOS application core libraries
* iOS application reference implementation

Our goal when open sourcing the code is to be transparent and establish
a dialog with the community.  Through this transparency and ongoing discussion,
our hope is to build trust and ensure any concerns raised are resolved before
solutions based on PEPP-PT are released to the general public.

## Contributing

The project does not accept contributions through GitHub at this point.

Details will be described in [CONTRIBUTING](./CONTRIBUTING.md).

## Questions or feedback

You may send questions or feedback to the
[PEPP-PT discussion group](https://groups.google.com/forum/#!forum/pepp-pt-discussion).

## License

This is an open-source project of [PEPP-PT](https://www.pepp-pt.org/).  It is
licensed under the [MPL](./LICENSE.txt) by the original copyright holders.  See
[LICENSE](./LICENSE.txt) and [CONTRIBUTORS](./CONTRIBUTORS.txt).
