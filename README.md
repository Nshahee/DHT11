# DHT11

**Testing a DHT11 (Temperature and Humidity) sensor's functionality and accuracy**



**General Sensor Information:**<br />

-Required voltage 3.5-5V<br />
-3 input sensor Power, Ground, data output<br />
-Averages around 3$<br />
-Digital output sensor<br />
-Communicates 8 bit signals to arduino<br />
-Response time averages around 10s<br />

**Temperature Sensor Information:**<br />
-Range: 0-50 ℃<br />
-Accuracy: ±2℃<br />
-Uses an NTC thermistor <br />
-1℃ resolution<br />

**Humidity Sensor Information:**<br />
-Range: 20%-90% RH (Relative Humidity)<br />
-Accuracy: ±5% RH<br />
-±1% RH accuracy per year<br />
-Uses a resistive polymer to detect humidity<br />
-1% RH resolution<br />

**Hardware setup:**<br />
-3 nodes on the sensor are attached to their respective points in an arduino<br />
-Left node- outputs signals<br />
-Middle node- Vcc<br />
-Right node- Ground<br />

**Software:**<br />
Coded in arduino<br />
#include <dht.h><br />
dht DHT;<br />
#define DHT11_PIN 7<br />
void setup(){<br />
  Serial.begin(9600);<br />
}<br />
void loop(){<br />
  int chk = DHT.read11(DHT11_PIN);<br />
  Serial.print("Temperature = ");<br />
  Serial.println(DHT.temperature);<br />
  Serial.print("Humidity = ");<br />
  Serial.println(DHT.humidity);<br />
  delay(2000);<br />
}

**Experiment:**<br />
-The temperature sensor is sent into an air sealed box<br />
-To test the humidity, a spray bottle is used in a small hole providing mist into the closed system<br />
-To test temperature, a space heater is attached to a cup with an air sealed lid to add heat to the system<br />
-A more accurate digital sensor is used to provide result comparisons<br />

**Results:**<br />
After running the experiment once, the results found that since the two sensors were not aligned with each other in the closed space the air that they were measuring was different, so the trial was executed again with more precision. <br />

**Temperature results**

**Humiditity results**

