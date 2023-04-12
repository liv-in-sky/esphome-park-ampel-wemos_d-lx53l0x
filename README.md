# esphome-park-ampel-wemos_d1


auf youtube: https://www.youtube.com/shorts/nFh81V3uW6I

- hierbei handelt es sich um eine einparkhilfe (park hilfe/parking assistent) durch entfernungsmessung
- die anzeige folgt über 3 leds oder einem **ws2812b** led-stripe (6 leds)
- gebraucht wird ein wemos d1
- der entfernungsmesser ist ein **vl53l0x** sensor - es müßte auch für sr04 nutzbar sein, wenn umgeschrieben
- wird in iobroker genutzt und sendet mqtt daten (daher universelleinsetzbar

**wie funktioniert's ?:**
```diff
+ die meisten hier erwähnten settings sind unter substitutions einzustellen
+ led's werden nach definierter zeit abgeschalten
+ mqtt (distanz und farbe led) wird nur versendet, wenn led's farbe ändern oder ein unterschied der distanz von 0.2 m gemessen wird
+ die entfernungen für die ampelfarben muss eingestellt werden
+ die wifi angaben eingeben !
+ mqtt mit port eingeben
```
die farben sind leider durch die kamera nicht gut zu erkennen :-(

![script-vis38](https://user-images.githubusercontent.com/18462890/230928555-8c46efa4-f9e0-46fa-9033-b080795d0e93.gif)

Empfehlung - die led's mit einem längeren kabel anschliessen, da die messung für das auto tiefer vorgenommen wird

**pin anschlüsse:**
```diff
+ LED's
D3: rote led
D4: grüne led
D5: gelbe led
+ WS2812B
GPIO3: steuerkanal
```

![script-vis39](https://user-images.githubusercontent.com/18462890/230932528-7ad4125b-9e69-4034-8d14-4ef8dbd3b2ac.gif)

