# DigiDot_1

Lern Oase - Eine Idee für eine kindgerechte Sammlung spannender und lehrreicher Inhalte - Alles auf einen Blick in einer übersichtlichen Linkliste: Wissen, Spaß und Medien erklärt – für neugierige Kinder von heute!

Lern-Oase 🌱 – Wissensserien für Kids

Link zum Coder - https://github.com/Inormatophilus/DigiDot_1/blob/main/Lern_Oase.html

Link zum gehsoteten code mit git - https://raw.githack.com//Inormatophilus/DigiDot_1/main/Lern_Oase.html

Eine interaktive Single-Page-Application (SPA), die als kuratierte Bibliothek für Lern- und Wissensserien für Kinder dient. Die gesamte Anwendung ist in einer einzigen HTML-Datei gebündelt und nutzt reines (Vanilla) JavaScript für die Funktionalität.
<br>
<!-- FÜGE HIER EINEN SCREENSHOT ODER EIN GIF DEINER ANWENDUNG EIN -->

![alt text](https://user-images.githubusercontent.com/726976/189432457-3de431d1-1375-415f-86f7-b183660505b0.gif)

✨ Key-Features

    Interaktive Serien-Übersicht: Eine moderne, kartenbasierte Darstellung aller Wissensserien.

    Filter- & Suchfunktion: Filtere Serien nach Kategorien (z.B. Wissen, Geschichte, Die Maus) oder nutze die Live-Suche, um Titel und Beschreibungen zu durchsuchen.

    Zufallsentdeckung: Finde mit dem "🎲 Zufall"-Button eine zufällige Serie aus der aktuellen Auswahl.

    Detailansicht mit Episoden: Jede Serie hat eine eigene Detailseite mit Beschreibung, Ersteller und einer Liste aller zugehörigen Episoden.

    Direkte YouTube-Verlinkung: Jede Episode und jede Playlist ist direkt mit YouTube verknüpft und öffnet sich in einem neuen Tab.

    Eigene Serien hinzufügen: Über ein Modal-Fenster können Benutzer eigene Serien (z.B. private YouTube-Playlists) hinzufügen.

    Lokale Speicherung: Hinzugefügte Serien werden als "Favoriten" im localStorage des Browsers gespeichert und bleiben so dauerhaft erhalten.

    Responsives Design: Die Benutzeroberfläche ist für Desktops, Tablets und Smartphones optimiert.

    Moderne UI/UX: Ansprechende Animationen, Hover-Effekte und ein "Glassmorphismus"-Design sorgen für eine tolle Benutzererfahrung.

🚀 Technische Umsetzung

Dieses Projekt wurde bewusst ohne externe Frameworks (wie React, Vue oder Angular) und ohne Build-Tools umgesetzt. Alles, was du brauchst, ist ein Browser.
1. Struktur (HTML)

Die Anwendung ist als Single-Page-Application (SPA) konzipiert. Anstatt mehrere HTML-Dateien zu laden, werden Inhalte dynamisch in die Seite injiziert. Die Hauptstruktur besteht aus:

    #overviewPage: Die Startseite, die die Filter, die Suche und die Liste aller Serien (#seriesList) anzeigt.

    #detailPage: Eine Seite, die anfangs verborgen ist und die Details einer ausgewählten Serie (#seriesDetail) anzeigt.

    #addModal: Ein Pop-up-Fenster (Modal) mit einem Formular, um neue Serien hinzuzufügen.

    Die Navigation zwischen diesen Ansichten wird vollständig über JavaScript gesteuert.

2. Design (CSS)

Das Design ist ein zentrales Merkmal der Anwendung und wird durch umfangreiches, direkt in die HTML-Datei eingebettetes CSS realisiert.

    CSS-Variablen: Das gesamte Farbschema ist über :root-Variablen definiert, was eine einfache Anpassung des Designs ermöglicht.

    Glassmorphismus: Effekte wie backdrop-filter: blur() und halbtransparente Hintergründe erzeugen einen modernen "Milchglas"-Look.

    Flexbox & Grid Layout: Für die responsive Anordnung der Elemente werden moderne CSS-Layouts verwendet. Das .series-list-Raster passt sich automatisch an die Bildschirmbreite an.

    Animationen & Übergänge: Diverse @keyframes-Animationen (float, slideIn, ripple) und transition-Effekte sorgen für eine lebendige und flüssige UI.

    Pseudo-Elemente: ::before und ::after werden kreativ für Hintergrund-Overlays, Hover-Effekte und dekorative Elemente genutzt.

3. Funktionalität (JavaScript)

Die gesamte Logik der Anwendung wird durch Vanilla JavaScript gesteuert.

    Datenquelle: Die vordefinierten Serien sind in einem JavaScript-Array const serien gespeichert. Jede Serie ist ein Objekt.

    Dynamisches DOM-Rendering:

        Die Funktion displaySeries() filtert und durchsucht die Seriendaten und generiert dynamisch den HTML-Code für die Serienkarten.

        renderSeriesDetail() und renderEpisodes() erzeugen die Detailansicht, wenn eine Serie ausgewählt wird.

    State Management: Einfache Variablen wie activeFilter und searchQuery speichern den aktuellen Zustand der App.

    SPA-Navigation:

        Um ein seitenähnliches Erlebnis ohne Neuladen zu schaffen, wird die History API (window.history.pushState()) verwendet.

        Der popstate-Event-Listener sorgt dafür, dass der "Zurück"-Button des Browsers korrekt funktioniert.

    LocalStorage für Favoriten:

        Neue, vom Benutzer hinzugefügte Serien werden als JSON-String im localStorage gespeichert.

        Beim Laden der Seite werden diese Favoriten wieder ausgelesen und zur Liste hinzugefügt. Dies ermöglicht Persistenz ohne eine serverseitige Datenbank.

    Event-Handling: Event-Listener für Klicks (Filter, Buttons) und Eingaben (Suche) aktualisieren den Zustand und rufen die Rendering-Funktionen erneut auf, um die Ansicht zu synchronisieren.

🏁 Getting Started

Da dies ein reines Frontend-Projekt in einer einzigen Datei ist, ist der Start denkbar einfach:

    Klone dieses Repository:
    Generated bash

      
git clone https://github.com/DEIN-BENUTZERNAME/DEIN-REPO-NAME.git

    

IGNORE_WHEN_COPYING_START
Use code with caution. Bash
IGNORE_WHEN_COPYING_END

Navigiere in den Projektordner:
Generated bash

      
cd DEIN-REPO-NAME

    

IGNORE_WHEN_COPYING_START

    Use code with caution. Bash
    IGNORE_WHEN_COPYING_END

    Öffne die index.html-Datei in einem beliebigen modernen Webbrowser.

Das war's! Die Anwendung ist nun einsatzbereit.
🤝 Contributing

Beiträge sind willkommen! Wenn du Ideen für neue Features hast, Fehler findest oder Verbesserungen vorschlagen möchtest, erstelle bitte einen neuen Issue oder einen Pull Request.
