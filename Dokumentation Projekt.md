# Dokumentation – EF Projekt
### Ein Wassernapf, der vom Hund aufgefüllt wird

## Abstract
Mein Projekt ist ein Wassernapf für den Hund, der vom Hund selbst aufgefüllt werden kann. Durch einen Knopf kann der Hund Wasser in den Napf füllen lassen und der Code sorgt dafür, dass es keine Überschwemmung gibt und das Ventil sich früh genug selber schließt.

## Projekt im Detail 
#### Beschreibung 
Über einen Knopfdruck kann man ein Ventil öffnen, welches mit einem großen Wasserkanister verbunden ist. Das Wasser fließt in einen modifizierten Napf, der dafür sorgt, dass kein Wasser überschwappt. Dies funktioniert wie folgt; Im Napf sind zwei Kabel, welche getrennt voneinander sind, wenn der Wasserstand über beide Kabel gestiegen ist, leiten sie und der Arduino wird dazu beauftragt dafür zu sorgen, dass kein Wasser mehr durchgepumpt wird. Das Ventil wird durch ein Relais gesteuert, welches dem Ventil ermöglicht mit 12V angesteuert zu werden. Der Arduino Micro, den ich in diesem Projekt benutzt habe, ist nicht in der Lage so viel Volt auszusenden.

#### Features 
Grundsätzlich war es mir möglich alle geplanten Funktionen umzusetzen. Man kann per Knopfdruck das Ventil öffnen. Das Ventil geht nicht mehr auf, wenn der Wasserstand genug hoch ist, dass die Kabel einen Kreislauf durch das Wasser aufbauen.

#### Hardware 
Das wichtigste Teil ist das Relais. Ohne das Relais würde nichts funktionieren, da das Relais dafür sorgt, dass alles so zusammenspielen kann wie es sollte.
Das Ventil und der Knopf spielen beide natürlich auch eine wichtige Rolle, da ohne diese beiden Teile auch nichts funktioniert hätte, aber beide haben nicht so eine bindende Funktion wie das Relais.
Der Arduino Micro ist ein zentrales Teil, da ohne den Arduino das Projekt auch nicht zustande gekommen wäre. Der Arduino übernimmt die meiste Arbeit im ganzen Projekt.
(Breadboard Bild)

#### Software
Die Software funktioniert wie folgt; Alle wichtigen Pins werden am Anfang festgelegt. Danach wird einfach überprüft ob der Button gedrückt wird und ob der Sensor (die beiden Kabel im Napf) leiten oder nicht, wenn sie nicht leiten und man drückt kommt Wasser raus und wenn sie leiten kommt kein Wasser.

## Entwicklung Hardware
#### 07.02.2023
Am 07.02.2023 habe ich mir nur Gedanken gemacht, was ich überhaupt machen will. An diesem Nachmittag bin ich nur zum Entschluss gekommen, was ich machen will. Eine kleine und auch gleichzeitig die einzige Skizze habe ich gemacht. (Skizze1)

#### 14.02.2023
Ich habe mir überlegt welche Teile ich brauche und für was. Das Problem war, dass ich mir nicht genügend Gedanken gemacht habe und mir zuerst falsche Teile zusammen gesucht habe. An diesem Tag habe ich noch nicht mal die Bestellliste abgeschickt, weil ich nicht fertig war.

#### 21.02.2023
Eine Woche und ein Gespräch mit Herrn Saxer für ein EF-Wechsel später habe ich die Teile nun bestellt. In der letzten Woche und auch in dieser war der Selbstzweifel sehr hoch, die Uhr hat getickt und ich hatte Garnichts.

#### 28.02.2023
Die Teile sind endlich angekommen, jedoch das Relais was ich bestellt habe, war das Falsche. Ich habe ein 1-Wege-Solid-Relais bestellt, was unnütz war, da es nicht das machte, was das Relais eigentlich machen sollte, weil es der Falsche Typ Relais war. An diesem Nachmittag habe ich die 3 Lektionen nur verschwendet, da ich die ganzen 3 Lektionen damit beschäftigt war das Ventil zum Laufen zu bringen, aber es war nicht mal möglich, weil es das Falsche Relais war. (Relais Bild)

#### 07.03.2023
An diesem Nachmittag habe ich am Knopf gearbeitet. Dieser Nachmittag war der unproduktivste Nachmittag, weil ich innerhalb von 3 Lektionen nur 4 Zeilen Code geschrieben habe und den Knopf richtig verkabelt habe.

#### 14.03.2023
An diesem Nachmittag habe ich die Ventil-Schaltung mit einem Transistor geschalten. Es hat nicht funktioniert. An diesem Tag habe ich das richtige Relais bestellt; ein 1-Kanal Relais. An diesem Nachmittag habe ich Hardware und Code technisch nicht geschafft, jedoch war dieser Tag ein Erfolg, da ich das richtige Relais bestellt habe. (Richtiges Relais Bild)

#### 21.03.2023
An diesem Nachmittag habe ich angefangen mit dem richtigen Relais zu arbeiten, ich habe alles auf das Breadboard gesteckt und alles hat perfekt funktioniert. Die ganze Hardware hat auf dem Breadboard einwandfrei funktioniert. (Breadboard Bild)

#### 22.03.2023
An diesem Nachmittag habe ich alles zusammengelötet und mein Gehäuse gebaut. Meinen Code habe ich vom 21.03 zum 22.03 über die Nacht geschrieben. Als ich alles zusammengelötet habe hat sich das Relais selbstständig gemacht. Warum? Das konnte ich nach 2 Stunden testen und Spannung messen nicht herausfinden.

#### 23.03.2023
An diesem Tag habe ich alles nochmal neu zusammengelötet und es hat funktioniert so wie ich es wollte. Leider habe ich während dem Arbeiten am 22.03 und am 23.03 vergessen Bilder zu machen.

## Diskussion und Reflexion

#### Was hat gut/schlecht funktioniert?
Der Code hat sehr gut funktioniert, das einzige was mir noch Unsicherheit bereitet ist, da ich selbst nach austesten nie garantiert sicher war ob ich den Button-Pin == LOW oder == HIGH machen sollte. Manchmal hat er, wenn ich ihn nicht gedrückt habe im Serial.Print 1 angegeben und manchmal 0.
Die gesamte Hardware war ein grosser Krampf. Ich habe viele Fehler gemacht vor und nach dem zusammenlöten und musste am 23.03 ganze 10 Stunden im Makersspace verbringen, um zu basteln und löten. Oft sind mir Kabel gerissen, falscher Pin zusammengelötet, falsche Masse beim Gehäuse, falsches Relais und das Relais hat sich selbstständig gemacht
Und der Wille war auch ein grosses Problem. Ich war extrem demotiviert, weil es die ganze Zeit Fehler gab, und sehr oft wurde ich sogar ziemlich wütend während des Erbauens der Hardware, weil immer irgendetwas nicht geklappt hat. Wie weiter oben schon erwähnt kam es sogar so weit, dass ich zwischendurch sogar EF wechseln, da ich mir dort zumal und jetzt immer noch nicht ganz zutraue überhaupt einen genügenden Schnitt hinzubekommen.

#### Was würdest du anders machen?
Ich würde ein mehr Code-basiertes Projekt machen, weil mir das Schreiben des Codes deutlich besser gelungen ist und ich eigentlich nur Probleme an der Hardware hatte.

#### Wie könnte ich das Projekt verbessern?
Die Hardware verschönern und den Weg, um sicher zu gehen, dass der Napf nicht überlauft zu verschönern; mit einem Messgerät das den Wasserstand messen kann oder einer Wage.

## Code

```cpp
int buttonPin = 7;    // Pin, an dem der Knopf angeschlossen ist
int valvePin = A5;    // Pin, an dem das Ventil angeschlossen ist
int sensorPin = A0;   // Pin, an dem der Wasserstandssensor angeschlossen ist

int valveState = LOW; 

void setup() {
  pinMode(buttonPin, INPUT_PULLUP);
  pinMode(valvePin, OUTPUT);
  pinMode(sensorPin, INPUT);
  Serial.begin(9600);
}

void loop() {
  int buttonState = digitalRead(buttonPin);  // Lesen des Knopfzustands
  int sensorValue = analogRead(sensorPin);  // Lesen des Stromkreiszustands im Hundenapf

  if (buttonState == LOW) {  
    if (sensorValue < 800) {  // Wenn der Stromkreislauf im Hundenapf nicht geschlossen ist
      valveState = HIGH;  
    } else {  // Wenn der Stromkreislauf im Hundenapf geschlossen ist
      valveState = LOW;  
    }
  } else {  // Wenn der Knopf nicht gedrückt wird
    valveState = LOW;  
  }

  digitalWrite(valvePin, valveState);  // Ventilstatus aktualisieren

  Serial.print("Knopf: ");
  Serial.print(buttonState);
  Serial.print(", Sensor: ");
  Serial.print(sensorValue);
  Serial.print(", Ventil: ");
  Serial.println(valveState);

  delay(100);  // Kleine Verzögerung zur Entprellung
}


