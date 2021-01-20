# Notes about powering the Raspberry Pi 1B

## Power consumption
http://raspi.tv/2014/how-much-less-power-does-the-raspberry-pi-b-use-than-the-old-model-b

### Just Keyboard Dongle
B: 4.98 V, 0.38 A, 1.89 Watts

### Keyboard Dongle + Edimax Wifi Dongle
B: 4.98 V, 0.43 A, 2.14 Watts

### Amperage
roughly 0.425 Amps@5V


## Supercapacitors
voltage - 2.7 per piece => 2 in series

### What capacity to choose for 30-60s of runtime (safe shutdown)
| PSU max current @5V | 19A |
|-|-|
| max cap charge current | 15A |

### Calculations
http://mustcalculate.com/electronics/capacitorchargeanddischarge.php

from 5V to 4.2V @420mA
| capacity [F] | time [s] |
|-|-|
| 10 | 21 |
| 15 | 31 |

charging

from 0V to 5V, 0.5ohm resistor
| capacity [F] | peak current [A] | resistor wattage [W] | time [s] |
|-|-|-|-|
| 10 | 10.2 | 52 | 20 |
| 15 | 10.2 | 52 | 30 |

from 0V to 5V, 0.4ohm resistor
| capacity [F] | peak current [A] | resistor wattage [W] | time [s] |
|-|-|-|-|
| 10 | 12.75 | 65 | 16 |
| 15 | 12.75 | 65 | 23 |

