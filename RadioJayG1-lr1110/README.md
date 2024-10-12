RadioJay G1
===========

RadioJay bird tracker with GPS, LoRa radio, rechargeable battery, and solar cell.

GPS questions:
--------------

- is RTC xtal required, or can time be injected from uC?
- is power switch required or is low power mode sufficient? Key issue is dead battery cut-off and
  subsequent recharge profile
- use pure software control or use interface pins? (In both directions)
- need 1.8V Vreg?
