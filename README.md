# IOT
1)LED
https://wokwi.com/projects/333797276169273940
void setup() {
  pinMode(13,OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(7, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(3000);
  digitalWrite(13, LOW);
  delay(100);
digitalWrite(12, HIGH);
  delay(3000);
  digitalWrite(12, LOW);
  delay(100);
digitalWrite(7, HIGH);
  delay(3000);
  digitalWrite(7, LOW);
  delay(100);
}
