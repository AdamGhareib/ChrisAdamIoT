# Stuur een signaal van de ene NodeMCU naar de andere (via internet)

- Gemaakt door Christiaan Dirven 500847226 & Adam el Ghareib, 500849066
- 12 oktober 2022

# Introductie

In deze tutorial ga je leren 

# Benodigde hardware components

- 1x Arduino Board (ESP8266 Development Board)
- 1x Button

# Stap 1: Make a feed

Om de communicatie met Adafruit IO tot stand te kunnen brengen, moeten we wat extra libraries installeren met behulp van de Arduino 

1. Klik op de 3e tab (zie onderstaande afbeelding) 
2. zoek naar  Adafruit IO Arduino (by Adafruit) in in het zoekvak,
3. Install (kies Install All)
<img src="/images/InstallLibrary.png" width="375px">

# Stap 2: Install the button

Om gebruik te kunnen maken van Adafruit IO, moeten we eerst een account en een dashboard aanmaken. 

1. Ga daarvoor naar https://io.adafruit.com/ , klik op “Get Started for Free” en maak een account aan.  
2. In Adafruit IO: ga de gele sleutel in het menu
<img src="/images/ActivateKey.png">
3. Kopieer je key en username

# Stap 3: Upload & Verifiy the code

In adafruit IO

1. Dashboards > New Dashboard (Maak een dashboard aan)
2. Ga naar het dashboard
3. Create New Block  via:
<img src="/images/Settings.png" width="375px" alt="settings">
4. Kies color Picker
5. Create de feed name: color
6. Create Block
7. Stel een kleur in met de Color Picker

# Stap 4: Check the feed

1. In Arduino: File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
2. In tab ‘config.h’: plak je Adafruit IO username en Key in
3. In tab ‘config.h’: voer het wifi netwerk en wachtwoord in 
4. (De NodeMCU werkt niet op 5Ghz WiFi)
5. Gebruik liefst de hotspot van je telefoon, dit gebruikt < 0.1 Mb data per uur, dus niet bang zijn
6. in de Tab adafruit_14_Neopixel.ino
7. Pas: #define **PIXEL_PIN 5** aan naar #define **PIXEL_PIN D5**

# Errors:

Probleem:
<img src="/images/Error1.png">
<img src="/images/Error2.jpeg">

Oplossing:
<img src="/kjhuimages/Error3.png">

# Bronnen:

https://docs.google.com/document/d/13Dvwrig2d11fmS7UafYM0o4nzgMpfTHDadrS2Py0mg0/edit#
