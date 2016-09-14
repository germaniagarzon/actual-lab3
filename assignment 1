int ledgreenPin = 10;
int ledyellowPin = 9;
int ledredPin = 11;
int buttongreenPin = 4;
int buttonyellowPin = 2;
int buttonredPin = 7;
int pot = A1;
int buttongreenState = 0;
int buttonyellowState = 0;
int buttonredState = 0;
int sensorValue = 0;

void setup() {
  Serial.begin(9600);
  pinMode(ledgreenPin, OUTPUT);
  pinMode(ledyellowPin, OUTPUT);
  pinMode(ledredPin, OUTPUT);
  pinMode(buttongreenPin, INPUT);
  pinMode(buttonyellowPin, INPUT);
  pinMode(buttonredPin, INPUT);
}

void loop() {
  sensorValue = analogRead(pot);
 int  brightness = map(sensorValue, 0, 1024, 0, 255);
  buttongreenState = digitalRead(buttongreenPin);
  buttonyellowState = digitalRead(buttonyellowPin);
  buttonredState = digitalRead(buttonredPin);
  Serial.print("green button state: ");
  Serial.print(buttongreenState);
  Serial.print("yellow button state: ");
  Serial.print(buttonyellowState);
  Serial.print("red button state: ");
  Serial.print(buttonredState);
  Serial.print(", Sensor value: ");
  Serial.print(sensorValue);
  Serial.print(", brightnes: ");
  Serial.println(brightness);
  if (buttongreenState == HIGH) {
    analogWrite(ledgreenPin, brightness);
  } else {
  if (buttonyellowState == HIGH) {
    analogWrite(ledyellowPin, brightness);
  } else {
  if (buttonredState == HIGH) {
    analogWrite(ledredPin, brightness);
  } else {
    analogWrite(ledgreenPin, 0);
    analogWrite(ledyellowPin, 0);
    analogWrite(ledredPin, 0);
   }}}
}
