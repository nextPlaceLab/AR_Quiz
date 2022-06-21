# AR_Quiz

![Screenshot_20220210-145839_LLE AR-Quiz](https://user-images.githubusercontent.com/57839896/174756989-ebff13a1-a429-4203-9585-e400cd9abfa1.jpg)

## About

### USE CASE 1: AR-BASIERTES QUIZ-TOOL DURCH ERKENNUNG PLANARER FLÄCHEN

Aufgrund den Erfahrungen des AR-Stadtrundgangs wurden weitere Tracking-Verfahren erforscht, um eine bessere Nutzer:innenerfahrung im Umgang mit Augmented-Reality-Technologien zu ermöglichen. Im Folgenden wurde ein Prototyp realisiert 
bei dem das Platzieren der Hologramme nicht durch Image-Marker, sondern durch 
die Erkennung planarer Flächen funktioniert. Für die Umsetzung dieser mobilen Applikation wurde erneut die Entwicklungsplattform Unity3D verwendet. Ziel war es 
nun, eine plattformübergreifende Augmented-Reality-Anwendungen einschließlich 
zusätzlicher, internen Funktionen, wie nachfolgend beschrieben, umzusetzen und 
mit den verschiedenen Stakeholdergruppen zu testen.
Die Applikation startet mit einem Umgebungsscan der geräteinternen Kamera, 
die das Umgebungsbild nach Bereichen absucht, die als planare Flächen erkannt 
werden. Planare Flächen werden beispielsweise in zusammenhängenden Bodenoder Tischoberflächen oder auch bei Wänden und Decken digital identifiziert. Die 
Kernfunktion dieses Prototypen bestand in einer Kombination der unterschiedlich 
erkannten Flächenelemente mit einer überlagerten Einblendung jeweils individueller Frageformulare. Wird die erkannte Fläche mittels Touch-Geste auf dem Bildschirm markiert, erscheint an gleicher Stelle ein interaktives Quiz als Hologramm, 
das sich per Touch-Steuerung auf dem Display weiter bedienen lässt. Die eingegebenen Antworten werden an einen Server weitergeleitet. Die Inhalte des Quiz können 
variabel angepasst werden, so dass die Applikation in verschiedensten thematischen 
Kontexten eingesetzt werden kann. Eine, im Projekt beispielhaft umgesetzte, Einsatzmöglichkeit war ein thematisch angepasstes Quiz im Rahmen eines Workshops 
mit Kindern und Jugendlichen zum Thema Biodiversität. Aber auch bereits skizzierte 
Anwendungen, wie beispielsweise die Verwendung als Umfrage-Tool, wäre eine weitere, sinnvolle Nutzungsmöglichkeit.
Anders als bei den bisher genutzten Tracking-Verfahren werden hier keine sichtbaren Marker eingesetzt. Bei diesem Prototyp können keine Inhalte dauerhaft an 
gleicher Stelle verortet werden bzw. deren Standorte auf andere Geräte übermittelt 
werden. 
Jedoch erscheinen die Hologramme stabiler und ruhiger im Raum verortet zu sein, 
als bei der Anzeige mit Bild-Markern.

![Flowcharts für Publikation - 2 3  AR basiertes Quiz-Tool durch Erkennung planarer Flächen](https://user-images.githubusercontent.com/57839896/174757088-2a515aea-fcef-4cca-9da9-63c632686dc9.jpg)

### USE CASE 2: IOT & AR BASIERTE URBAN GARDENING ANWENDUNG

Bei der hier entwickelten IoT- & AR-basierten Anwendung für Urban-Gardening-Projekte handelt es sich um eine Kombination von Hardware und Software zur Unterstützung von gemeinschaftlichen Garten-Projekten in einem Stadtquartier. Der 
Kernaspekt der Anwendung ist die Übertragung von Sensordaten über LoRaWAN 
(Long Range Wide Area Network) und deren Visualisierung in einer Augmented-Reality-Applikation auf mobilen Endgeräten. Für die Umsetzung des Prototyps wurde 
das Netzprotokoll LoRaWAN eingesetzt. Damit können kleinere Datenpakete (z.B. 
Sensordaten) über größere Entfernungen (z.B. innerhalb eines Stadtquartiers) per 
Funkverbindung übertragen werden. Ein LoRaWAN benötigt einen Empfangsmodul 
(LoRa-Gateway), welches mit per WiFi bzw. per Ethernet mit einem IoT-Server verbunden ist. Darüber hinaus wird mindestens ein Sender (LoRa-Node) benötigt, von 
dem die Daten an das Empfangsmodul übertragen werden. 
Im ersten Schritt wurde das LoRa-Gateway mit dem Standort am Standort der Essigfabrik in Köln bei der Plattform "The Things Network" registriert, um den Zugriff 
auf nötige IoT-Server-Funktionen zu erhalten (siehe obere Abbildung). Im zweiten 
Arbeitsschritt wurde ein LoRa-Node als Prototyp aufgesetzt. Dieser besteht im 
Wesentlichen aus einem Mikrocontroller (Arduino-Uno), mehreren Sensoren (u.a. 
Temperatur, Luftfeuchtigkeit) und einem LoRa-Shield (Sender + Antenne). Nach der 
Programmierung (z.B. Auslesen & Übersenden der Sensordaten) bzw. der entsprechenden Konfiguration (u.a. Einstellung der Frequenzbänder) beider Geräte, können 
Datenpakete der Sensoren über das LoRaWAN an den IoT-Server geschickt werden 
und dort abgerufen werden. Für die Umsetzung der mobilen Applikation wurde 
erneut die Entwicklungsplattform Unity verwendet. Diese Entwicklungsumgebung 
wurde ausgewählt, weil sich plattformübergreifende Augmented-Reality-Anwendungen mit internen Funktionen realisieren lassen und weil eine Schnittstelle zum 
IoT-Server durch einen quelloffenen Softwarebaustein (M2MQTT for Unity) mit verhältnismäßig geringem Aufwand hergestellt werden kann. 
Um die grundlegenden Konzepte der Applikation testen zu können, wurde die Funktionsweise wie nachfolgend beschrieben implementiert: Beim Start der Applikation scannt die geräteinterne Kamera die Umgebung und markiert Bereiche, die als 
planare Flächen erkannt wurden. Beim Drücken auf das Display (bzw. auf einen Bereich in den markierten planaren Flächen) erscheint an dieser Stelle ein Hologramm 
und es wird eine Verbindung zum IoT-Server aufgebaut von dem (Sensor-)Daten abgerufen werden. Das Hologramm stellt eine Visualisierung dieser Daten dar. Im 
bisherigen Prototyp wurden die Daten auf Servern eines Dienstleisters gehostet. 
Das Hosten der Daten auf eigenen Server-Strukturen sollte zukünftig in Betracht gezogen werden. In anderen Nutzungskontexten, außerhalb der Thematik des Urban 
Gardening, könnte ein Prototyp dieser IoT/AR-Anwendung mit Cloud Anchors auch 
für Umfragen mit stationären Fragebögen eingesetzt werden.

![Flowcharts für Publikation - 3 1  IoT  amp; AR basierte Urban Gardening Anwendung](https://user-images.githubusercontent.com/57839896/174757430-7dc73ce1-ec98-47f7-9b53-d53b4bd6d248.jpg)
