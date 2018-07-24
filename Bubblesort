// NeoPixel Ring simple sketch (c) 2013 Shae Erisson
// released under the GPLv3 license to match the rest of the AdaFruit NeoPixel library

#include <Adafruit_NeoPixel.h>
#ifdef __AVR__
#include <avr/power.h>
#endif

// Which pin on the Arduino is connected to the NeoPixels?
// On a Trinket or Gemma we suggest changing this to 1
#define PIN            4

// How many NeoPixels are attached to the Arduino?
#define NUMPIXELS      6

// When we setup the NeoPixel library, we tell it how many pixels, and which pin to use to send signals.
// Note that for older NeoPixel strips you might need to change the third parameter--see the strandtest
// example for more information on possible values.
Adafruit_NeoPixel pixels = Adafruit_NeoPixel(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);

int delayval = 500; // delay for half a second

void setup() {
  // This is for Trinket 5V 16MHz, you can remove these three lines if you are not using a Trinket
#if defined (__AVR_ATtiny85__)
  if (F_CPU == 16000000) clock_prescale_set(clock_div_1);
#endif
  // End of trinket special code

  pixels.begin(); // This initializes the NeoPixel library.
  Serial.begin(9600);
}

void loop() {

  // For a set of NeoPixels the first NeoPixel is 0, second is 1, all the way up to the count of pixels minus one.
  int r0=128, g0=0,   b0=128;
  int r1=4,   g1=0,   b1=208;
  int r2=0,   g2=255, b2=0;
  int r3=255, g3=255, b3=0;
  int r4=255, g4=100, b4=0;
  int r5=255, g5=0,   b5=0;
  int rw=255, gw=255, bw=255;

  int x[] = {
    0,1,2,3,4,5    };

    while(x[5] == 5) 
    {
    const size_t n = sizeof(x) / sizeof(x[0]);

    for (size_t i = 0; i < n - 1; i++)
    {
      size_t j = random(0, n - i);

      int t = x[i];
      x[i] = x[j];
      x[j] = t;
    }
  }
  
  for(int i = 0; i < 6  ; i++)
  {
    Serial.println(x[i]);
  }

  pixels.setPixelColor(x[0], pixels.Color(r0,g0,b0));
  pixels.setPixelColor(x[1], pixels.Color(r1,g1,b1));
  pixels.setPixelColor(x[2], pixels.Color(r2,g2,b2));
  pixels.setPixelColor(x[3], pixels.Color(r3,g3,b3));
  pixels.setPixelColor(x[4], pixels.Color(r4,g4,b4));
  pixels.setPixelColor(x[5], pixels.Color(r5,g5,b5));
  pixels.show(); 

  delay(delayval);

  int i, j,tmp;

  for (i = 0; i < 6 ; i++) 
  {
    pixels.setPixelColor(x[0], pixels.Color(r0,g0,b0));
    pixels.setPixelColor(x[1], pixels.Color(r1,g1,b1));
    pixels.setPixelColor(x[2], pixels.Color(r2,g2,b2));
    pixels.setPixelColor(x[3], pixels.Color(r3,g3,b3));
    pixels.setPixelColor(x[4], pixels.Color(r4,g4,b4));
    pixels.setPixelColor(x[5], pixels.Color(r5,g5,b5));
    pixels.show(); 
    delay(1000);
    for (j = i; j < 6 ; j++) 
    {
      if (x[i] > x[j]) 
      {
        tmp = x[i];
        x[i] = x[j];
        x[j] = tmp;
      }
    }
  }

  pixels.setPixelColor(x[0], pixels.Color(r0,g0,b0));
  pixels.setPixelColor(x[1], pixels.Color(r1,g1,b1));
  pixels.setPixelColor(x[2], pixels.Color(r2,g2,b2));
  pixels.setPixelColor(x[3], pixels.Color(r3,g3,b3));
  pixels.setPixelColor(x[4], pixels.Color(r4,g4,b4));
  pixels.setPixelColor(x[5], pixels.Color(r5,g5,b5));
  pixels.show(); 
  delay(3500);
  
  
  pixels.setPixelColor(x[0], pixels.Color(rw,gw,bw));
  pixels.setPixelColor(x[1], pixels.Color(rw,gw,bw));
  pixels.setPixelColor(x[2], pixels.Color(rw,gw,bw));
  pixels.setPixelColor(x[3], pixels.Color(rw,gw,bw));
  pixels.setPixelColor(x[4], pixels.Color(rw,gw,bw));
  pixels.setPixelColor(x[5], pixels.Color(rw,gw,bw));
  pixels.show(); 
  delay(1500);

}

