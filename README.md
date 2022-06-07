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

2) colour RGB
3) https://wokwi.com/projects/333801225781772882
4) 
int red_light_pin= A5;
int green_light_pin = A4;
int blue_light_pin = A3;
void setup() {
  pinMode(red_light_pin, OUTPUT);
  pinMode(green_light_pin, OUTPUT);
  pinMode(blue_light_pin, OUTPUT);
}
void loop() {
  RGB_color(0, 255, 255); // red
  delay(1000);
  RGB_color(0, 0, 255); // yellow
  delay(1000);
 RGB_color(255, 0 , 255); // green
  delay(1000);
}
void RGB_color(int red_light_value, int green_light_value, int blue_light_value)
 {
  analogWrite(red_light_pin, red_light_value);
  analogWrite(green_light_pin, green_light_value);
  analogWrite(blue_light_pin, blue_light_value);
}
