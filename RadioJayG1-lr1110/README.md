RadioJay G1 - LR1110
====================

Test & dev board for LR1110, which provides GPS snapshot functionality as well as LoRa radio.
A STM32U083 is used as microcontroller for its low power features, familiarity with its peripherals,
and its 256KB flash, which can be used to store GPS data.

The main purpose of the board is to prototype all the pieces and be able to measure power consumption.

Open questions while designing the board:
- Is it possible to get away without 900Mhz RF switch, as one can with the stm32wle?
  The stm32wle datasheet has a footnote in the "sub-Ghz radio characteristics" stating
  "When not in RX operation mode up to 22 dBm is accepted [on RFI_P/RFI_N]". Neither the
  sx1262 nor the lr1110 datasheet have this note so it's not clear whether this is a feature added
  by ST when integrating the sx1262 or whether it's something Semtech doesn't feel the need to specify.
- Can the GPS LNA power be supplied by the LR1110, eliminating one awkward to route signal. The
  datasheet doesn't specify max source current but it does spec minimum V-high voltage @2.5mA,
  which is the typ consumption of the LNA (max is 3.5mA).
- What are the power consumption implications of having only one 32.768kHz xtal and routing the
  clock from the stm32u083 to the LR1110?
- Would rotating the stm32u883 improve the routing?
- What are the minimum RF test points needed in the "final" tag?
