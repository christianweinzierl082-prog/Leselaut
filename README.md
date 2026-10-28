# LeseLaut – Android-Vorlese-App

Eine einfache Android-App, die gedruckten Text aus einem Foto erkennt und auf Deutsch vorliest.

## Funktionen
- Foto mit der Kamera aufnehmen
- Bild aus Galerie/Dateiauswahl wählen
- OCR-Texterkennung mit Google ML Kit (lateinische Schrift)
- Erkannter Text kann vor dem Vorlesen bearbeitet werden
- Deutsche Android-Sprachausgabe
- Vorlesen, Pause, Weiter und Stopp
- Einstellbare Lesegeschwindigkeit

## In Android Studio öffnen
1. ZIP entpacken.
2. Android Studio öffnen und **Open** wählen.
3. Den Ordner `LeseLautAndroid` auswählen.
4. Gradle-Synchronisierung abwarten.
5. Ein Android-Gerät per USB mit aktivierten Entwickleroptionen verbinden oder einen Emulator starten.
6. Auf **Run** klicken.

## Hinweise
- Dieses Paket enthält den Android-Quellcode, keine bereits kompilierte APK.
- Für den Bau wird Android Studio mit JDK 17 und Android SDK Platform 35 benötigt.
- Die Sprachausgabe verwendet die auf dem Gerät installierte Android-TTS-Engine. Wenn keine deutsche Stimme installiert ist, installiere deutsche Sprachdaten über die Android-Einstellungen (Text-in-Sprache-Ausgabe).
- Die ML-Kit-Texterkennung wird beim ersten Einsatz ggf. über Google Play Services bereitgestellt.
- Das Projekt ist ein Ausgangspunkt und wurde in dieser Umgebung nicht auf einem echten Android-Gerät gebaut oder getestet.


## APK automatisch erstellen (ohne Android Studio auf dem eigenen PC)
Das Projekt enthält einen GitHub Actions-Workflow unter `.github/workflows/android-apk.yml`.
Lade den entpackten Projektordner als Repository zu GitHub hoch. Öffne anschließend im Repository
**Actions → Build LeseLaut APK → Run workflow**. Nach erfolgreichem Build findest du unter dem
abgeschlossenen Lauf das Artefakt **LeseLaut-debug-apk**. Lade es herunter, entpacke es und
installiere `app-debug.apk` auf deinem Android-Gerät. GitHub-Konto und Internetverbindung sind
dafür erforderlich. Der Workflow wurde hier nicht ausgeführt; ein erfolgreicher Build ist daher
noch nicht bestätigt.
