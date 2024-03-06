# Arduino
Ampelschaltung-läuft-zyklisch
LF7: Ampelprojekt Arduino
Ampelprojekt Arduino

Little Arduino Project, only for school purposes only.
Erstellen Sie ein GIT-Repository und bearbeiten folgende Entwicklungsschritte.
Jede Neuergänzung und Tests werden in Branches ausgelagert.

Jede Neuergänzung und Tests werden in Branches ausgelagert.
1) Ampelschaltung läuft zyklisch durch
2) Fußgängerampel implementieren
3) Bedarfsanmeldung mittels Push-Button
4) Ton-Signal, wenn die Fußgängerampel grün zeigt
5) Kopplung des Bedarfrufs von zwei Straßenseiten.



Aufgabe: 

int switchState = 0;
void setup() {
 // put your setup code here, to run once:

pinMode (3, OUTPUT);
pinMode (4, OUTPUT);
pinMode (5, OUTPUT);
pinMode (2, INPUT);

}

void loop() {
  // put your main code here, to run repeatedly:

switchState = digitalRead(2);
if (switchState == LOW)   {  //the button is not pressed

digitalWrite (3,LOW);     //green LED
digitalWrite (4,LOW);     //red LED
digitalWrite (5,LOW);     //yellow LED
  }


else { // the button is pressed
digitalWrite (3,LOW);    
digitalWrite (4,HIGH);    
digitalWrite (5,HIGH);

delay (250);   //wait for a quarter second
// toggle the LEDs
digitalWrite (4,HIGH);    
digitalWrite (5,LOW);    
delay (250);  //wait for a quarter second
    
  }
 // go back to the beginning of the loop

}
