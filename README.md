### Test Webprogrammierung 29.05.2024

**Name:**

**Anweisungen:** Beantworten Sie alle Fragen sorgfältig und vollständig. Die maximale Punktzahl für diesen Test beträgt 130 Punkte.

---

#### Teil 1: Planung eines Webprojektes (Relaunch)

**1.1.** Welchen wesentlichen Unterschied gibt es zwischen dem Relaunch einer bestehenden Webseite und der Planung einer neuen Webseite? (5 Punkte)

Bei einem Relaunch bestehen bereits Analyse-Daten von der bestehenden Website, man kann sich dabei die wichtigsten Kriterien herausnehmen und ausarbeiten. Dabei zu beachten ist allerdigngs auch, dass man dabei alle wichtigen Kriterien beachtet. SEO beispielsweise spielt dabei eine große Rolle, man möchte natürlich dass die derzeitigen Websitenutzer dei Seite weiterhin nutzen und finden. Bei einem Relaunch kann es sein dass sich URLs oder auch die Domain ändert und Einfluss auf SEO auslöst. Bei der Planung einer neunen Website begint man von 0, baut alles von neu auf und muss nicht auf bestehendes achten. Allerdings gibt es keine Analyse-Daten an die man sich halten kann.

**1.2** Beschreiben Sie die wesentlichen Schritte bei der Planung eines Website-Relaunchs. (10 Punkte)

- Website- und Markenanalayse
- Definition eines übergeordneten Ziels der Website
- Definition kleinerer Ziele
- Definition Prioritäten
- Erstellung des Briefings
- Entscheidung für einen Dienstleister
- Website-Konzeption und Erstellung des Designs
- Evtl. Entscheidung für ein CMS
- technische Umsetzung
- Testing und Anpassungen
- Launch und Nachjustierungen

**1.3** Warum ist es wichtig, eine Bestandsaufnahme der aktuellen Website durchzuführen? Nennen Sie zwei Gründe. (5 Punkte)

- Aus einer Bestandsaufnahmen der aktuellen Website können wichtige Analysedaten gesammelt und für die neue Website verwendet werden. 
- Damit es zu keinem Konflikt im SEO Bereich während eines Relaunches kommt, ist es wichtig, interne Verlinkungen, Back-Links, Meta-Title und Meta Description zu kennen, diese für die neue Website anzupassen bzw. zu überprüfen ob sie automatisch wieder korrekt erstellt oder angepasst werden müssen.
- Es ist wichtig die Inhalte zu kennen, zu entscheiden, welche werden weiter verwendet, welche nicht und was wird neues benötigt. Dabei ist auch wichtig abzuklären, ob die Inhalte exportiert werden können. Im Gesamten kann dadurch ein manueles Anpassen von Inhalten im Nachhinein vermieden werden. 

**1.4** Welche Rolle spielt die Zielgruppenanalyse bei einem Website-Relaunch? (5 Punkte)

Die Zielgruppenanalyse spielt eine der wichtigsten Rollen bei einem Website-Relaunch. Die Website wird explizit für die Zielgruppe erstellt und sollte diese daher auch optimal ansprechen. Ein Website-Relaunch sollte vor allem auf den Inhalt ausgerichtet sein, weshalb es wichtig ist diesen auch an die Zielgruppe anzupassen. 

---

#### Teil 2: Git und Github

**2.1** Erklären Sie, was Git ist und wofür es verwendet wird. (5 Punkte)

Git ist ein Versionskontrollprogramm, welches vor allem für die Verwaltung von Quellcode in Softwareentwicklungsprojekten verwendet wird. Ein Versionskontrollprogramm speichert jegliche Änderungen, welche an einem Projekt vorgenommen werden. Zu einem späteren Zeitpunkt kann auch immer auf alle verschiedenen Versionen des Projekts zugegriffen und zurückgekehrt werden.

**2.2** Was ist Github und wie unterscheidet es sich von Git? (5 Punkte)

Github ist eine Web-basierte Oberfläche, welche die Verwaltung von Git-Repositorys ermöglicht. Github ermöglicht ebenfalls die Arbeit in verschiedenen Arbeitszeigen (Branches), welche es perfekt ermöglichen, im Team zu arbeiten. Gitbub ist somit ein sehr geeignetes Verwaltungstool, aber auch ein Tool für das Projektmanagement und Hosting von Projekten. 

**2.3** Erklären Sie jeden der folgenden Begriffe: (10 Punkte)

* Repository: Projekt, Projektordner
* Branch: Arbeitszweig, im Team kann jeder auf einem eigenen Branch arbeiten und am Ende werden wieder alle in den main-banch zusammengefasst
* Commit: Mit einem Commit werden einige Änderungen zusammengefasst und im lokalen Repository gespeichert. (Neue Version erstellt)
* Merge: Arbeitszweige, also Branches, werden zusammengeführt
* Fetch: Das lokale Projekt wird aktualisiert, alle Änderungen werden geladen, sollten neue Commits/andere Projektmitarbeiter also etwas gepusht haben, sind diese nun ersichtlich
* Pull: alle Projektänderungen werden in das lokale Projekt geladen, somit ist das lokale auf dem selben Stand wie das im Web
* Push: Commits aus dem lokalen Projekt werden hochgeladen in das Web-Repository
* Clone: Beim Clonen wird ein Web-Repository verknüpft heruntergeladen, und kann lokal bearbeitet und mit dem Web-Repository synchronisiert werden
* Remote Repository / Origin: Ein Remote Repository ist ein lokales Repository, welches mit einem anderen zuammengeführt werden kann.
* Konflikt: Konflikte sind Probleme, welche beim pushen von Commits entstehen

---

#### Teil 3: CSS-Variablen nutzen

**3.1** Was sind CSS-Variablen und warum sind sie nützlich? (5 Punkte)

CSS-Variablen werden im root angelegt, und können Werte speichern. Nützlich sind diese Variablen, wenn Werte mehrmals benötigt werden. Fallen Änderungen an, können diese in den Variablen erstellt werden und der Wert wird überall(wo die Variable verknüpft wurde) automatisch aktualisiert.

**3.2** Überarbeite den folgenden CSS-Code, indem du redundante Werte identifizierst und entscheidest, welche in CSS-Variablen ausgelagert werden sollten. Achte auf sinnvolle Variablennamen. (10 Punkte)

```css

:root {
  --color-light-grey: #f0f0f0;
  --color-dark-grey: #333;
  --color-white: #ffffff;
  --color-blue: #007bff;
  --font-arial: Arial;
  --distance-20: 20px;
  --fs-button: 16px;
  --width-card: 300px;
}

/* Farben */
body {
  background-color: var(--color-light-grey);
}

.header {
  background-color: var(--color-dark-grey);
  color: var(--color-white);
}

.button {
  background-color: var(--color-blue);
  color: var(--color-white);
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

.card {
  background-color: var(--color-white);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  padding: 20px;
}

/* Schriftarten */
h1 {
  font-family: var(--font-arial), sans-serif;
}

p {
  font-family: var(--font-arial), sans-serif;
}

/* Abstände */
.container {
  margin: var(--distance-20);
}

.header {
  padding: var(--distance-20);
}

.card {
  margin-bottom: var(--distance-20);
}

/* Größen */
.button {
  font-size: var(--fs-button);
}

.card {
  width: var(--width-card);
}

```

---

#### Teil 4: Komponentenbasierte Elemente für Websites entwickeln

**4.1** Was versteht man unter komponentenbasiertem Webdesign? (5 Punkte)

Dabei werden Komponenten oder auch verschiedene Websitenelement (z.b. ein Text-Bild Element) erstellt, welche immer wieder verwendet werden können, sobald sie benötigt werden. Sie besitzen somit denselben Aufbau, dieselben Klassen und IDs und können durch eine einmalige Gestaltung alle gemeinsam und gleich gestaltet werden. 

**4.2** Nennen Sie zwei Vorteile der Nutzung von komponentenbasierten Elementen. (5 Punkte)

- Komponenten können wiederverwendet werden, Code muss nicht mehrmals geschrieben werden und es wird somit Zeit gespart.
- Durch die weiderverwendung, haben Komponenden den selben Aufbau, dieselben Klassen und IDs, und können somit alle gemeinsam formatiert werden

**4.3** Erstellen Sie ein einfaches Beispiel für eine komponentenbasierte HTML-Struktur (Kartenkomponente mit Bild, Titel, Text). (10 Punkte)

```html
<!-- Beispiel HTML-Struktur für eine Kartenkomponente -->

<div class="card">
  <div class="card__image">
    <img clas="cardImage__image" src="" alt="">
  </div>
  <div class="card__content">
    <h2 class="card__title">Title</h2>
    <p class="card__text">Text</p>
  </div>
</div>

```

---

#### Teil 5: Container Queries

**5.1** Was sind Container Queries und wie unterscheiden sie sich von Media Queries? (5 Punkte)

Container Queries sind eine Möglichkeit für responsives Webdesign. Der Unterschied zu den Media Queries ist, dass Media Queries als Referenz immer die Viewportbreite verwednen, Container Queries hingegen die Containerbreite. 

**5.2** Beschreiben Sie eine Situation, in der Container Queries besonders nützlich sein können. (5 Punkte)

Wenn ich zwei Container habe, die nebeneinander angeordnet sind. In einem Container sind alle hauptinformationen enthalten, im danebenstehenden Container Nebeninformationen. Der Container mit den Hauptinformationen soll immer gleich dargestellt werden. Aus Platzgründen im responsiven Design soll der Inhalt des zweiten Containers allerdings ab einer bestimmten Contianergröße untereinander angeordnet werden. 

**5.3** Erweitern Sie den folgenden **CSS-Code** um eine Container Query, sodass der Innenabstand eines Elements bis zu einer Containerbreite von 400px (width) 20px beträgt. (10 Punkte)

```css

.container {

}

.box {
  padding: 40px;
}

/* Container Query */

@contianer (max-width: 400px) {
  
  .box {
    padding: 20px;
  } 

}

```

```html
<div class="container">
  <div class="box">
    Dies ist eine Beispiel-Box mit variabler Schriftgröße.
  </div>
</div>
```

---

#### Teil 6: Praktische Aufgabe

Sie erhalten ein bestehendes Webprojekt auf Github und sollen einen Relaunch planen und teilweise umsetzen. Gehen Sie wie folgt vor: (30 Punkte)

0. Erstellen Sie ein Repository "Aufgabe6-Webprog" auf Ihren lokalen Rechner und kopieren Sie den Inhalt aus dem Ordner "Daten" hinein.
1. Erstellen Sie den "initial commit"
2. Erstellen Sie einen neuen Branch mit dem Namen "relaunch".
3. **Durchführen der folgenden Änderungen:**
   - **CSS-Variablen:** Definieren Sie sinnvolle CSS-Variablen und verwenden Sie diese in Ihrer CSS-Datei.
   - **Komponentenbasierte Elemente:** Entwickeln Sie eine einfache, komponentenbasierte HTML-Struktur für eine Kartenkomponente, die einen Titel, ein Bild und einen Text enthält.
   - **Container Queries:** Implementieren Sie eine Container Query, um die Schriftgröße der Kartenkomponente basierend auf der Containergröße anzupassen. Verwenden Sie eine Schriftgröße von 1rem bis zu einer Containerbreite von 540px.
4. **Committen Sie Ihre Änderungen:** Geben Sie nach jedem bedeutenden Schritt einen aussagekräftigen Commit-Namen an und committen Sie Ihre Änderungen.
5. **Merge:** Führen Sie einen Merge des "relaunch"-Branches zurück in den Haupt-Branch ("main") durch.
6. Erstellen Sie auf ihrem Github-Account ein neues öffentliches Repository mit dem Namen "Abgabe-Webprog".
7. Notieren Sie hier die URL zu Ihrem Repo auf Github: https://github.com/vanessainn/Abgabe-Webprog
8. Pushen Sie Ihr lokales Repository in das neu erstellte Remote-Repository.
9. Speichern Sie zusätzlich alle lokalen Dateien als ZIP-Datei "vorname-nachname.zip" und mailen diese an manuel@startmedia.at