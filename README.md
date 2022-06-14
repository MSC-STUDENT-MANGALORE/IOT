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
https://wokwi.com/projects/333801225781772882

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
  RGB_color(255, 255 , 0); // blue
  delay(1000);
  RGB_color(255, 255, 255); // black
  delay(1000);
  RGB_color(0, 0 , 0); // white
  delay(1000);
  
}
void RGB_color(int red_light_value, int green_light_value, int blue_light_value)
 {
  analogWrite(red_light_pin, red_light_value);
  analogWrite(green_light_pin, green_light_value);
  analogWrite(blue_light_pin, blue_light_value);
}


DISPLAY
lcd 16*4 i2c
https://wokwi.com/projects/333806275695477332
/* Hello Wokwi! */

#include <LiquidCrystal_I2C.h>

LiquidCrystal_I2C lcd(0x27, 20, 4);

void setup() {
  lcd.init();
  lcd.backlight();
  lcd.setCursor(1, 0);
  lcd.print("Hello, Wokwi!");
}

void loop() {
  lcd.setCursor(7, 1);
  lcd.print(millis() / 1000);
}


RGB l2
void setup() {
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
  
}

void loop() {
  displayColor(0b100); //RED
  delay(1000);
  displayColor(0b010); //GREEN
  delay(1000);
  displayColor(0b001); //BLUE
  delay(1000);
  displayColor(0b101); //MAGENTA
  delay(1000);
  displayColor(0b011); //CYAN
  delay(1000);
  displayColor(0b110); //YELLOW
  delay(1000);
  displayColor(0b111); //WHITE
  delay(1000);
}

void displayColor(byte color) {
  digitalWrite(13, !bitRead(color, 2));
  digitalWrite(12, !bitRead(color, 1));
  digitalWrite(11, !bitRead(color, 0));
}
https://wokwi.com/projects/333806427979121235

