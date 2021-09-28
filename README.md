# Lab-4-Control---Sherry-s-Part-
//"arms"
unsigned long currentMillis;
unsigned long previousMillis = 0;

#include <Servo.h>

Servo myservo;  
Servo myservo1;

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
  myservo1.attach(10); 
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    myservo1.write(pos); 
    delay(30);    
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    myservo1.write(pos); 
    delay(5);                      
  }
}

//"HAND" for FastLED
#include <FastLED.h>

// How many leds in your strip?
#define NUM_LEDS 64

// For led chips like WS2812, which have a data line, ground, and power, you just
// need to define DATA_PIN.  For led chipsets that are SPI based (four wires - data, clock,
// ground, and power), like the LPD8806 define both DATA_PIN and CLOCK_PIN
// Clock pin only needed for SPI based chipsets when not using hardware SPI
#define DATA_PIN 12
#define CLOCK_PIN 13

// Define the array of leds
CRGB leds[NUM_LEDS];

void setup() { 
    FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);  // GRB ordering is assumed
}

void loop() { 
  // Turn the LED on, then pause
  leds[7] = CRGB::Blue;
  leds[8] = CRGB::Blue;
  leds[23] = CRGB::Blue;
  leds[9] = CRGB::Blue;
  leds[10] = CRGB::Blue;
  leds[5] = CRGB::Blue;
  leds[21] = CRGB::Blue;
  leds[2] = CRGB::Blue;
  leds[12] = CRGB::Blue;
  leds[20] = CRGB::Blue;
  leds[13] = CRGB::Blue;
  leds[14] = CRGB::Blue;
  leds[16] = CRGB::Blue;
  leds[39] = CRGB::Blue;
  leds[40] = CRGB::Blue;
  leds[55] = CRGB::Blue;
  leds[56] = CRGB::Blue;
  leds[41] = CRGB::Blue;
  leds[53] = CRGB::Blue;
  leds[59] = CRGB::Blue;
  leds[34] = CRGB::Blue;
  leds[45] = CRGB::Blue;
  leds[50] = CRGB::Blue;
  leds[61] = CRGB::Blue;
  leds[33] = CRGB::Blue;
  leds[62] = CRGB::Blue;
  leds[47] = CRGB::Blue;
  leds[48] = CRGB::Blue;
  leds[36] = CRGB::Blue;
  leds[43] = CRGB::Blue;
  leds[52] = CRGB::Blue;
  FastLED.show();
  delay(3000);
  // Now turn the LED off, then pause
  leds[7] = CRGB::Black;
  leds[8] = CRGB::Black;
  leds[23] = CRGB::Black;
  leds[9] = CRGB::Black;
  leds[10] = CRGB::Black;
  leds[5] = CRGB::Black;
  leds[21] = CRGB::Black;
  leds[2] = CRGB::Black;
  leds[12] = CRGB::Black;
  leds[20] = CRGB::Black;
  leds[13] = CRGB::Black;
  leds[14] = CRGB::Black;
  leds[16] = CRGB::Black;
  leds[39] = CRGB::Black;
  leds[40] = CRGB::Black;
  leds[55] = CRGB::Black;
  leds[56] = CRGB::Black;
  leds[41] = CRGB::Black;
  leds[53] = CRGB::Black;
  leds[59] = CRGB::Black;
  leds[34] = CRGB::Black;
  leds[45] = CRGB::Black;
  leds[50] = CRGB::Black;
  leds[61] = CRGB::Black;
  leds[33] = CRGB::Black;
  leds[62] = CRGB::Black;
  leds[47] = CRGB::Black;
  leds[48] = CRGB::Black;
  leds[36] = CRGB::Black;
  leds[43] = CRGB::Black;
  leds[52] = CRGB::Black;
  FastLED.show();
  delay(500);
}

//"Smile" for FastLED
#include <FastLED.h>

#define NUM_LEDS 64

#define DATA_PIN 12
#define CLOCK_PIN 13

CRGB leds[NUM_LEDS];

void setup() { 
    FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);
}

void loop() { 
  leds[21] = CRGB::Yellow;
  leds[18] = CRGB::Yellow;
  leds[39] = CRGB::Yellow;
  leds[41] = CRGB::Yellow;
  leds[53] = CRGB::Yellow;
  leds[59] = CRGB::Yellow;
  leds[60] = CRGB::Yellow;
  leds[50] = CRGB::Yellow;
  leds[46] = CRGB::Yellow;
  leds[32] = CRGB::Yellow;
  FastLED.show();
  delay(1500);
  
  leds[21] = CRGB::Black;
  leds[18] = CRGB::Black;
  leds[39] = CRGB::Black;
  leds[41] = CRGB::Black;
  leds[53] = CRGB::Black;
  leds[59] = CRGB::Black;
  leds[60] = CRGB::Black;
  leds[50] = CRGB::Black;
  leds[46] = CRGB::Black;
  leds[32] = CRGB::Black;
  FastLED.show();
  delay(500);
}
