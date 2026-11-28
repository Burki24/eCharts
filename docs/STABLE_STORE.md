# Erste Stable-Einreichung von eCharts

Die veröffentlichte Beta 1.431 (Commit `f3a6b1408076ae0e15c127848a716bbf0187c889`)
ist der fachliche Ausgangspunkt. Die folgenden Texte beschreiben den Umfang
für die erste Stable-Einreichung. Version und Veröffentlichungsdatum sind offen.

## Angaben für beide Sprachen

| Store-Feld | Eintrag |
| --- | --- |
| Vorhandenes Bundle | `de.burki24.symconecharts` |
| Name | eCharts |
| Zielkanal | Stable |
| Repository | `https://github.com/Burki24/eCharts` |
| Kategorien | Informationen, Visualisierung |
| Lokalisierungen | Deutsch (`de`), Englisch (`en`) |
| Mindestversion | Symcon 9.0 |
| Dokumentation DE | [README.md](../README.md) |
| Dokumentation EN | [README.en.md](../README.en.md) |

Für die Store-Felder den vollständigen SHA des geprüften Release-Commits auf
`main` verwenden. Die Dokumentationslinks haben die Form
`https://github.com/Burki24/eCharts/blob/<SHA>/README.md` (DE) und
`https://github.com/Burki24/eCharts/blob/<SHA>/README.en.md` (EN).
Die endgültige Versionsnummer aus der `library.json` dieses Commits in beide
Versionsinformationen übernehmen. Das tatsächliche Veröffentlichungsdatum gehört
nach der Freigabe in den Stable-Eintrag im [Changelog](../CHANGELOG.md).
Die markierte Beta-Überschrift wird unabhängig davon weitergeführt.

## Deutsch

### Beschreibung

eCharts zeigt aktuelle Messwerte, Archivverläufe und Beziehungen zwischen
Symcon-Objekten. Die Bibliothek enthält 32 Diagrammmodule und ein gemeinsames
Gateway. Du kannst zum Beispiel die Leistungen mehrerer PV-Flächen stapeln,
Fensterzustände auf einer Zeitachse vergleichen oder die Windrichtung auf
einer drehbaren Windrose ablesen. Für Symcon-Kacheln und IPSView stehen eigene
Designer mit Vorschau bereit. Apache ECharts und die Themes werden mitgeliefert.

### Versionsinformation

Erste Stable-Ausgabe. Wer bereits die Beta nutzt, kann die eingerichteten
Instanzen und ihre Quellen weiterverwenden. Zeitreihen und historische Balken
unterstützen gestapelte Archivwerte. GaugeWind bietet 37 Windrosen und eigene
SVG-Motive. Beim Kopieren des Kacheldesigns nach IPSView zeigt die Vorschau
auch ungespeicherte Änderungen an. Mit **Übernehmen** speicherst Du den Entwurf.

Bestehende JSLive-Diagramme lassen sich über Exportpakete des Vertrags 1.0
übernehmen. Das Gateway zeigt die Quellenzuordnung und Darstellungsabweichungen
vor der Bestätigung. Die Übernahme legt neue Diagramme an und verwendet die
zugeordneten Quellen und deren vorhandene Archivwerte. Das JSLive-Original
bleibt erhalten.

## English

### Description

eCharts displays live readings, historical measurements and relationships between
Symcon objects. The library includes 32 chart modules and one shared gateway.
You can stack the power output of several solar arrays, compare window states
on a timeline or read the wind direction on a rotating compass rose. Symcon
tiles and IPSView each have a designer with a preview. Apache ECharts and its
themes are bundled with the library.

### Release notes

First stable release. If you already use the beta, you can keep your configured
chart instances and sources. Time series and historical bar charts support
stacked archive values. GaugeWind offers 37 compass rose presets and accepts
custom SVG artwork. Copying a tile design into IPSView previews unsaved changes.
Select **Apply** to save the draft.

You can import existing JSLive charts using migration packages in contract
version 1.0. The gateway shows source assignments and visual differences before
you confirm. Importing creates new charts using the assigned sources and their
available history. The original JSLive chart is preserved.

## Hinweise zum Review

Der Zugriff auf mitgelieferte Grafiken, die installierte Symcon-Iconbibliothek
und die exportierte Zigbee2MQTT-Netzwerkkarte ist lesend. Die JSLive-Neuanlage
erfordert eine ausdrückliche Bestätigung. Der Skriptaufruf `ECTR_SetTreeJSON`
schreibt das geprüfte Dokument nur im JSON-Modus und lehnt ausstehende
Konfigurationsänderungen ab. Die Designkopie bearbeitet den Formularentwurf.

Die [bisherigen Abnahmen und offenen Testvarianten](BETA_STORE.md#einordnung-der-verbleibenden-hinweise)
gelten weiterhin. Insbesondere sind Touchgeräte, weitere Plattformvarianten
und mehrstündige Last- und Speicherläufe nur teilweise abgedeckt.
