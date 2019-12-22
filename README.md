# thermometer-DHT22-TM1637
This is simple digital thermometer and humidity meter based on ATTINY 13 / ATTINY 85 , digital LED module TM1637 and sensor DHT22 (AOSONG AM2302 module). Supports negative temperatures measurement (-40 up to + 80 Celsius) and better resolution ( 0.5 degree)

The code for DHT11 reading (modified for DHT22 sensor) and TM1637 display was borrowed from Łukasz Podkalicki : https://blog.podkalicki.com/attiny13-reading-temperature-and-humidity-from-dht11/ and https://blog.podkalicki.com/attiny13-tm1637-library/
Both libraries work flawless. Thank You Lukasz for good work.

Part List :

1 x ATTINY 13 / ATTINY 13A - ATMEL chip

1 x TM1637 4 digits module

1 x DHT22 humidity & temperature sensor (16bit resolution and negative temperatures available)

1 x LM7805 voltage stabilizer ( if not powered from 5V)

1 x 1N4007 diode ( if not powered from 5V, optional)

1 x 470 uF - 2200 uF electrolitic capacitor (optional, but gives stability of measurements)

1 x 47nF - 470nF capacitor (optional, but gives stability of measurements)


Connection to be made : Mandatory : all components - ATTINY 13 , TM1637 , DHT 22 - have to be connected to VCC 5V and GND line ( I am using LM7805 to provide stable +5V power for all components).

Optional : Between 5V and GND please put 100nF capacitor. At the input of LM7805 please put electrolityc capacitor and diode to protect LM7805 from inverted voltage.

The mandatory connections :

ATTINY 13 - VCC is pin #8, GND is PIN #4

DHT 22 - VCC is PIN #1, GND is PIN #4

TM1637 - VCC / 5V is PIN #1, GND is PIN #2

Add some capacitor like 100nF between 5V VCC and GND

connections from ATTINY13 to DHT22 and LED module :

DHT 11 sensor - DATA LINE - connect to PB4 ( PIN #3 ) on ATTINY 13

TM1637 module - DIO LINE - connect to PB0 ( PIN #5 ) on ATTINY 13

TM1637 module - CLK LINE - connect to PB1 ( PIN #6 ) on ATTINY 13

That's all. The code is ~950 bytes long after compilatiion. Must be compiled by AVR-GCC environment on Linux or Windows.
