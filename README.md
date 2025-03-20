# FaceRace4microbit
Tensorflow.js webcam classifier that connects to micro:bit and sends predictions over usb serial or Bluetooth.


https://vilvite.github.io/FaceRace4microbit/facerace.html

Testing log in Norwegian for my colleagues:

/*connect over BT VIRKER! 
! iPad tillater dessverre ikke web bluetooth APIen som brukes. ;_;
! Android må pares med enheten med A+B+Reset, så må man resette litt til den dukker opp som "BBC micro:bit" og ikke som f.eks [ZUZAV]
! Paring i Windows er på finspråket a hot mess! Ting går fort gale. Ser ut som at USB-tilkobling til PCen og paring/ikke-paring i nettleseren påvirker ting.
   Ting jeg gjør som får ting til å til slutt virke (micro:bit står i PC med USB)
    1) Steng nettleser, trekk ut ledning fra mb
    2) Åpne facerace.html, plugg i og sett mb i paringmodus
    3) Par mb i windows, men ha "Bluetooth & other devices" åpen
    4) Forsøk å pare mb i pairing-modus i nettleseren. Den skal dukke opp som BBC micro:bit [xxxxx]
    5) Reset mb. Se om den dukker opp som BBC micro:bit
    6) Hopp tilbake til Bluetooth & Other devices, be maskinen GLEMME micro:bit [xxxxx]
    7) Forsøk å pare med "BBC micro:bit" i nettleseren.
    8) Reset og prøv igjen til det funker?

micro:bit V1.0 gir 020 OUT OF MEMORY error om man prøver å legge til både BitBot-biblioteket og Bluetooth. Kitronik MOVE er ukompatibel.
Skal teste med V2.0 og se hvilke extensions som er kompatible. Krysser fingrene!
*/
