# FaceRace4microbit
Teachable Machine webcam classifier that connects to micro:bit and sends predictions over usb serial or Bluetooth.


https://vilvite.github.io/FaceRace4microbit/facerace.html

Testing log in Norwegian for my colleagues:

V 2.0 - 16.7.25
Har fikset problemene med at modellen leste helt feil. Viste seg at jeg dekodet bildene som rene Tensorflow-modeller i stedet for Teachable Machine-modeller. Usikker på hvilken metode som er lettest å fortsette med, håpet er å lage en modelltrener som kan kjøre på mobile enheter. Klarer nå å styre en bil med knyttneven og føler meg godt fornøyd!

V 1.5 - 23.3.25
Video kan speiles, men etter å ha testet med stillbilder vha OBS Virtual Cam ser jeg at modellen ikke tolkes på samme måte som ved trening på teachablemachine. Kan ikke se hva som kan være feil, må undersøke tensorflow-APIet mer (ChatGPT har hjulpet godt men virker tom for ideer).

V 1.4 - 20.3.25
Blåtann-kontakt virker! Det er en del ting å være obs på, dog:

 - iPad tillater dessverre ikke web bluetooth APIen som brukes. ;_;
 - Android må pares med enheten med A+B+Reset, så må man resette litt til den dukker opp som "BBC micro:bit" og ikke som f.eks [ZUZAV] 
 - Paring i Windows er på finspråket a hot mess! Ting går gale. Ser ut som at USB-tilkobling til PCen og paring/ikke-paring i nettleseren påvirker ting, og prøver du å koble til mens windows er paret til micro:biten, smelter Chrome. Eller micro:bitten flimrer og gir 020 OUT OF MEMORY.

   Ting jeg gjør som får ting til å til slutt virke (micro:bit står i PC med USB)
    1) Steng nettleser, trekk ut ledning fra mb
    2) Åpne facerace.html, plugg i og sett mb i paringmodus
    3) Par mb i windows, men ha "Bluetooth & other devices" åpen
    4) Forsøk å pare mb i pairing-modus i nettleseren. Den skal dukke opp som BBC micro:bit [xxxxx]
    5) Reset mb. Se om den dukker opp som BBC micro:bit
    6) Hopp tilbake til Bluetooth & Other devices, be maskinen GLEMME micro:bit [xxxxx]
    7) Forsøk å pare med "BBC micro:bit" i nettleseren.
    8) Reset og prøv igjen til det funker? micro:biten ser ut til å portene for å lytte etter kontakter, så om det er mange BT-enheter i nærheten som hilser på, gir den 020 memory error etter noen få sekunder! Anbefaler å forsøke å pare enhetene en og en på rolige dager.

micro:bit V1.0 gir 020 OUT OF MEMORY error om man prøver å legge til både BitBot-biblioteket og Bluetooth. En V2 klarer det fint. Bluetooth-biblioteket tar stor plass!

Kitronik MOVE er ukompatibel med Bluetooth.

Anbefaler BT på Android (telefon, for å flexe) og USB på PC. Face Race var tenkt med USB-seriell til micro:bit som radio-kobler til en annen micro:bit i en BitBot.

