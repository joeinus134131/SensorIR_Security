/*
 * program untuk pengujian sensor
 * edited 19 sept 2020
 * create by IDNmakerspace Algorithm Factory
 */
 
#include<Servo.h>

Servo myservo;
#define pinin A0

float datamasuk;
int pos = 0;
void setup() 
{
  
  Serial.begin(9600);
  pinMode(pinin, INPUT);
  myservo.attach(9);
}

void loop() 
{
  datamasuk = analogRead(pinin);
  Serial.print("Data masuk : ");
  Serial.println(datamasuk);
  if(datamasuk <= 100)
  {
    for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
    }
    for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  }
  else
  {
    Serial.println("Motor tidak masuk");
  }
  delay(100);
}
