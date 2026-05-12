Die [**Absaugung**](https://github.com/makerspace-wi/Absaugung-Lasercutter) geht automatisch beim Lasern an und wird mit 60 Sek. Nachlauf abgeschaltet

![Laser-Absaugung](.attachments.441096/absaugung%20%282%29.jpg)

#### Laserinnenraum

- Das Licht im Laser ist an der Seitenleiste an- und abschaltbar (siehe weiter unten)
- Beim CO2-Laser wird der Laserstrahl über drei Linsen geleitet (siehe unten)
  - Deren Reinigung und Austausch erfolgt durch das Technik-Team
- Hilfslaser: ein kleiner roter Laserpunkt, der beim Ausrichten hilft

![Die drei Linsen ](.attachments.441096/linsen.png)

![kleiner Ausrichtungslaser](.attachments.441096/roter_laser%20%284%29.jpg)

### **Kalibrierung:**

- Im Regal befinden sich die Kalibrierblöckchen (pink+gelb)
- Nimm das Blöckchen, das die Dicke deines Werkstückes hat und leg es auf dein Werkstück
- Richte auf der X- und y-Achse den Laserkopf über die Pfeiltasten auf dem Bedienpanel aus (2. Bild, Nr.1)
- Die z-Achse bzw. das Laserbett wird an der rechten Seite vom Laser verstellt (up/ down). Hier ist auch das Licht für den Laser zu finden (3. Bild)
- Für die richtige Höhe liegt der Laserkopf so auf dem Blöckchen auf, dass man gerade noch ein Blatt Papier zwischen Laserkopf und Blöckchen bewegen könnte

###### 

**GRAVIEREN:**

- der Laserkopf wird nicht mehr ausgetauscht. Stattdessen wird der Laserkopf zum Kalibrieren mit dem Gravurblöckchen ausgerichtet.
  - für eine Gravur ist die Materialdichte irrelevant, da der Fokuspunkt der Linse auf der Oberfläche liegen muss
  - für sehr feine Gravurarbeiten ist der Diodenlaser vorzuziehen

![Höheneinstellung](.attachments.441096/kalibrierung.jpg)

![Bedienpanel](.attachments.441096/controller_.jpg)

![Laserbettverstellung + Licht](.attachments.441096/h%C3%B6henverstellung.jpg)

#### Bedienpanel

- der Laser ist nicht per default eingeschaltet, er muss händisch am Knopf rechts unten eingeschaltet werden (hier aufpassen, es ist sehr schnell passiert, dass der Laser dann startet, aber man vergessen hat, den Laserstrahl auch anzuschalten)
- Während diese Lampe leuchtet und die Maschine sich bewegt, soll die Brille getragen werden
- als Sicherheitsmaßnahme wird der Laser, sobald die Klappe geöffnet ist, automatisch ausgeschaltet
  - ausschalten kann man den Laserstrahl nicht über seinen Knopf, mit Öffnung der Klappe ist er automatisch aus
- Im Notfall auf den Not-Aus-Knopf drücken

  ![Laser an](.attachments.441096/laser_an.jpg)

![Klappe offen - Laser ist automatisch aus](.attachments.441096/bedienplatte%20%283%29.jpg)

#### Danach

- Klötzchen etc zurückstellen
- Späne, Schnipsel etc. vom Lasern entfernen, da Brandgefahr!
- Logbuch zurücklegen

---

# PC & Lightburn

#### Dokumentenablage

- Um den PC sauber zu halten, legt euch bitte eigene Ordner unter “Dokumente” an.
- Um zu testen, welche Einstellungen bei eurem Werkstück die besten sind, gibt es dort einen Ordner für Kalibrierung. Dort gibt es Test Cards, die ihr an eurem Werkstück oder ähnlichem Material, verwenden könnt. Diese Test Cards gibt es für Gravur oder Schnitte. 
- Diese Karten sind so eingestellt, dass sie verschiedene Intensitäten und Geschwindigkeiten abdecken, sodass die gewünschte Leistung direkt anhand des Laserbildes ablesbar ist.

![Testkarten](.attachments.441096/Testkarten.png)

#### Laser-Einstellungen

- Ihr könnt eurem Stück verschiebene Ebenen mit unterschiedlichen Einstellungen zuweisen. 
- 1\. Jeder Ebene ordnet ihr eine Zahl zu
- 2\. Als Modi gibt es Linie (Schneiden) und Füllen (Gravur)
- 3\. Geschwindigkeit und Leistung könnt ihr an zwei Stellen einstellen, indem ihr auf die Zahl bei Geschwindigkeit/Leistung drückt, oder die Zahlen mittig rechts eingebt. Hier wird auch die Anzahl der Durchgänge eingegeben
  - *Tipp:* eine Differenz von 15 zwischen min und max Leistung lassen. (In Kurven wird der Laser langsamer, infolgedessen sollte die Leistung reduziert werden, um dort potentiell auftretende und unschöne Verkokelungen zu meiden)
  - Mehr Power, um Zeit zu sparen ist nicht zwingend gut. A) Verbrennungen an der Ober- und Unterseite des Werkstücks sind nicht hübsch, B) Ineinanerzusteckende Teile sind dadurch stabil, dass sie sehr akkurat gelasert werden, was zu viel Verbrennung verhindert, C) Zu viel Power und damit Dünstungen machen die Laserlinse kaputt
- 4: Toggles:
  - Ausgabe: diese Ebene (bzw diese Farbe) wird beim Lasergang ausgespart, also nicht gelasert 
  - Anzeigen: diese Ebene wird visuell ausgeblendet (ggf hilfreich für Fokus beim Ausrichten o.Ä.. aber Achtung: auch ausgeblendetes kann gelasert werden!)
  - Air Assist (Luftabsaugung) grün lassen
- **5: Ausgangsposition:** Der Laser wurde bereits physisch ausgerichtet, jetzt wird die Ausgangsposition festgelegt. Dafür wählt im Dropdown “Aktuelle Position” aus und dann einen der neun Punkte bei Job-Ausgangspositionen. Von hier wird der Laser navigiert.

  Das grüne Quadrat auf eurem Laserbild in Lightburn (Mitte) zeigt euch eure gewählte Job-Ausgangsposition an. 

  **__Große Fehlerquelle__**: Der von euch positionierte Laser wird abhängig von der ausgewählten Job-Ausgangsposition bewegt. Wenn ihr den Laser und euer Werkstück z.B. unten links positioniert habt, die Job-Ausgangsposition allerdings oben rechts eingestellt habt, navigiert der Laser nach links und unten, läuft in einen Error und lasert dabei ggf. euer Werkstück und/oder das Laserbett.
- 6: Senden: Schickt nun eure Datei mit allen Infos an den Laser. Den Namen (LIGHTBRN) nicht ändern, wir wollen den Speicherplatz nicht zumüllen.
  - *Tipp*: In der Icon-Reihe könnt ihr auf den Monitor klicken und bekommt dann eine Anzeige, wie lange der Laservorgang etwa dauern wird. Das ist nicht immer komplett akkurat, aber ein sehr guter Richtwert)  

![Lightburn](.attachments.441096/Lightburn.png)

![Min Max Durchgänge in der anderen Sicht](.attachments.441096/Min%20Max%20Durchg%C3%A4nge.png)

#### Bedienpanel

- 1: Nachdem der Laser ausgerichtet und dessen Ausgangsposition festgelegt wurde, wird dem Laser durch Drücken auf “Origin” auch mitgeteilt, dass diese Ausrichtung gerade sein Startpunkt ist
- 2: Über Frame wird von dort aus ein Rahmen um den Bereich, in dem eure Laserdatei liegt, gefahren, sodass ihr die Tatsächliche Größe seht. 
  - Tipp: Wenn ihr am Laser rechts das Licht ausschaltet, seht ihr den kleinen roten Ausricht-Laser und damit sehr gut die zu lasernde Fläche
- 3: Mit Start kann es jetzt endlich beginnen. (Vor dem Drücken geht immer nochmal sicher, dass auf dem Laser die “Laser scharf-Lampe” leuchtet
- Auf dem Panel wird jetzt beim Lasern nachgezeichnet, welche Strecke schon gelasert ist und wie viel Prozent abgeschlossen sind.

![Control Panel](.attachments.441096/Control%20Panel.png)

#### 