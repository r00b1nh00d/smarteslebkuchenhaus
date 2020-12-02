# Smartes Lebkuchenhaus
## ~avatar avatar @unplugged
Ein kleines Lebkuchenhaus in der Weihnachtszeit backen ist eine super Wochenendbeschäftigung. <br>
Zum backen kannst du dieses Rezept nutzen: <br>
![Rezept](https://github.com/r00b1nh00d/smarteslebkuchenhaus/blob/master/LebkuchenHausRezept.PNG?raw=true) <br>
Bei der Verzierung kannst du alles nutzen, was dir gefällt. Kekse, Gummibärchen, Schokolinsen uvm.

## ~@unplugged
Wie du siehst haben wir es hier mit der Deko wohl etwas zu gut gemeint :-D
![Haus](https://github.com/r00b1nh00d/smarteslebkuchenhaus/blob/master/LebkuchenHausBild.PNG?raw=true)

## ~@unplugged
Doch was hat jetzt die Informatik mit dem Lebkuchenhaus backen zu tun? <br>
Naja mit der Calliope kannst du dein Lebkuchenhaus etwas "Smart" machen. Sicher hast du schonmal von dem Begriff Smart Home gehört. <br>
Allgemein beteutet Smart Home, dass alle elektronischen Geräte im Haus mit einander Vernetzt sind und oft auch mit dem Internet verbunden sind. Ein Aspekt des Smart Homes ist es auch, wenn du z.B. dein Zuhause verlässt, dies erkannt wird und eine Steuereinheit zum Energiesparen das Licht ausschaltet. 

## Schritt 1
Wie bei der Alarmanlage für die Keksdose kannst du jetzt auch den Lichtsensor nutzen um die am Calliope verbaute RGB-LED oder auch weitere LED's bzw. Neopixel Anschalten zu lassen, sobald die gemessene Lichtstärke unter einen bestimmten Wert fällt.


```blocks
basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.setLedColor(0xffff00)
    } else {
        basic.setLedColor(0x000000)
    }
})
```
