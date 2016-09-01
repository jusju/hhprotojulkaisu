# Julkaisu HH proto-palvelimille Macillä

Tämä on ohje Mac-käyttäjille jotka haluavat julkaista protojaan Haaga-Helian proto-palvelimille. Ohjeessa käytetään Cyberduck-sovellusta WinSCP:n korvikkeena ja muokataan Cyberduckin yhteysasetukset kurssilla jaetun hhprotojulkaisu -ohjeen mukaan. 

Alkuperäisen ohjeen linkki (GitHub) https://github.com/jusju/hhprotojulkaisu/blob/master/README.md


Ladataan Cyberduck ja viedään latautunut sovellus Applications -hakemistoon.
Käynnistetään sovellus. Aloitusnäkymä näyttää tältä:

![kuva1](https://github.com/tpolvinen/hhprotojulkaisu/blob/master/kuvat/screen-capture-3.png)

Valikosta File valitaan "Open connection..." jolloin sovellusikkunan eteen ilmestyy avattavan yhteyden asetukseien ikkuna. Kuvassa ei ole vielä tarvittavia asetuksia:

![kuva2](https://github.com/tpolvinen/hhprotojulkaisu/blob/master/kuvat/screen-capture-4.png)

- Valitaan pudotusvalikosta yhteyden protokollaksi "SFTP (SSH File Transfer Protocol)".
- Kenttään "Server:" kirjoitetaan halutun protopalvelimen osoite (nimi vaihtelee kursseittain, joten tarkastakaa se opettajalta). Ohjeessa käytetään osoitetta "proto383.haaga-helia.fi".
- Portin numero jätetään oletusarvoonsa "22".
- Kenttään "Username:" kirjoitetaan oma tunnus, jonka pitäisi olla muotoa "a123456" ja salasanaksi sama kuin muuallakin, esim. Moodleen ja s-postiin kirjauduttaessa.
- Ohjeen kuvassa on jätetty täppä päälle kohtaan "Add to Keychain", mikä vähentää naputtelua mutta ei ole välttämätön toiminnan kannalta.
- Naksautetaan painiketta "Connect" 

![kuva3](https://github.com/tpolvinen/hhprotojulkaisu/blob/master/kuvat/screen-capture-5.png)

Yhteyden avauduttua avautuu tiedostonäkymä kohteen hakemistoon /home/a123456 (tunnusriippuvainen hakemistonimi), missä tulee navigoida hakemistoon "/var/lib/tomcat8/webapps": 

- Valitse keskellä näkyvästä palkista hakemistoksi "/" jolloin saat näkymään yläkansion sisällön.

![kuva4](https://github.com/tpolvinen/hhprotojulkaisu/blob/master/kuvat/screen-capture-6.png)

- Navigoi webapps -hakemistoon ja raahaa aikaisemmin Eclipsessä Export-toiminnolla tekemäsi WAR-tiedosto ikkunaan, jolloin tiedonsiirto käynnistyy automaattisesti.

Kun tiedosto on siirtynyt, tulee vielä näkyviin ikkuna, jossa näkyvät tiedonsiirron yksityiskohdat.

![kuva5](https://github.com/tpolvinen/hhprotojulkaisu/blob/master/kuvat/screen-capture-7.png)

Huomaa myös hhprotojulkaisu -ohjeen noudatettavat käytännöt:
"Tarkastele sovellustasi selaimen kautta miltä tahansa koulun koneelta. Vaihda proton numeron kohdalle kurssinne proton numero. Tuotos näkyy vain koulun verkossa. Laita projektin nimeksi sama kuin Eclipsessä on projektinne nimi."
