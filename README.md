# esphome-park-ampel-wemos_d1

- hierbei handelt es sich um eine entfernungsmessung als einparkhilfe (park hilfe/parking assistent)
- die anzeige folgt über 3 leds oder einem **ws2812b** led-stripe (6 leds)
- gebraucht wird ein wemos d1
- der entfernungsmesser ist ein **vl53l0x** sensor - es müßte auch für sr04 nutzbar sein 
- wird in iobroker genutzt und sendet mqtt daten (daher universelleinsetzbar

**wie funktioniert's ?:**
```diff
+ die meisten hier erwähnten settings sind unter substitutions einzustellen
+ led's werden nach definierter zeit abgeschalten
+ mqtt wird nur versendet, wenn led's farbe ändern
+ die entfernungen für jede ampelfarbe muss eingestellt werden
```
die farben sind leider durch die kamera nicht gut zu erkennen :-(
![script-vis38](https://user-images.githubusercontent.com/18462890/230928555-8c46efa4-f9e0-46fa-9033-b080795d0e93.gif)
