RadioJay Hardware Design
========================

This repo has various hardware designs for RadioJay wildlife tracking tags.
The first few were called "Mostag" for "Motus Open Source TAG" and then later rebranded to RadioJay.
The tags are listed here more or less in reverse chronological order.

For write-ups about these tags see the [RadioJay](https://radiojay.org) web site.

### RadioJay G1 - LoRaWAN+GPS tag

This is a collection of test & dev boards using a bit more space and with connectors to
attach probes and to swap between solar panels and GPS modules.

- [RadioJayG1-ublox](./RadioJayG1-ublox/) has a U-Blox Mia-M10Q GPS and an stm32wle5
  microcontroller with integrated LoRa radio.
- [RadioJayG1-lr1110](./RadioJayG1-lr1110/) has an LR1110 radio with snapshot GPS and with LoRa
  support and uses an stm32u083 microcontroller.
- [RadioJayG1-aem](./RadioJayG1-aem/) is a solar + battery module using an e-Peas AEM10330 energy
  harvesting chip with integrated buck converter; it can be used with a PowerFilm or an IXOLAR
  solar cell and with a LiPO or an LTO battery.
- [RadioJayG1-lr1110](./RadioJayG1-lr1110/) is a solar/battery module using an IXOLAR solar cell
  with an MPP volatge of 4.4V allowing direct charge without boost converter; it has a low Iq
  buck converter to output 1.8V

### RadioJay A2 / MostagV2

First real tag using FlexPCB with a target weight of 1g all-in (incl. loop harness).
Uses uC, Nichicon battery, PowerFilm solar, bq25504, and accelerometer
as well as altimeter (barometer)

![RadioJay A2](MostagV2/MostagV2.jpg)

#### RadioJay A2a / MostagV2a

Same board with layout changes to satisfy OSH Park's design rules.

### PgmAdapterV2

Adapter board for programming RadioJay A2MostagV2 using a simple USB-serial adapter chip.
Has connectors to attach various types of programming/debug probes.
Most likely not what "normal users" will use, but useful for development.

![PgmAdapterV2](PgmAdapterV2/PgmAdapterV2.jpg)

### RadioJay A1 / MostagV1

Initial proof of concept board, not for strapping to any animal, has uC,
Seiko battery, PowerFilm solar cell, bq25504, and accelerometer, plus linx antenna.

![RadioJay A1](MostagV1/TestTagV1-front.png)
