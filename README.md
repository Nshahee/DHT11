# DHT11

**Testing a DHT11 (Temperature and Humidity) sensor's functionality and accuracy**<br />

![Capture](https://user-images.githubusercontent.com/118258337/201899130-bd39c6a1-0162-44bc-96b9-6426570f8720.PNG)<br />

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
![2](https://user-images.githubusercontent.com/118258337/201899137-d170e5f8-f6fe-49cc-b320-3db9231a80ff.PNG)<br />
![3](https://user-images.githubusercontent.com/118258337/201899142-50202ab7-c8d7-40f2-ae24-dbe55a55e741.PNG)<br />

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
![4](https://user-images.githubusercontent.com/118258337/201899149-62725f83-86a2-40ce-9968-7a7f04788760.PNG)<br />
![5](https://user-images.githubusercontent.com/118258337/201899161-38cf52dd-1574-4b38-bb63-26c0d2cbd47c.PNG)
![6](https://user-images.githubusercontent.com/118258337/201899184-1f4416de-d661-449d-be66-13e2d9272f04.PNG)<br />

**Results:**<br />
After running the experiment once, the results found that since the two sensors were not aligned with each other in the closed space the air that they were measuring was different, so the trial was executed again with more precision. <br />

**Temperature results**<br />
![8](https://user-images.githubusercontent.com/118258337/201899198-d86f3c3e-cf85-4b51-bf67-ff5656646988.PNG)<br />

**Humiditity results**<br />
![7](https://user-images.githubusercontent.com/118258337/201899195-b8f44788-4e50-41c8-8635-2b1d155db734.PNG)<br />

**Resolution of sensor**<br />
Temperature:<br />
![9](https://user-images.githubusercontent.com/118258337/201899206-2808a1c0-d918-42b9-ac2c-7f4fcfb928d7.PNG)
![12](https://user-images.githubusercontent.com/118258337/201899235-eb404060-4451-483b-b213-514616293b8e.PNG)<br />

Humidity<br />
![10](https://user-images.githubusercontent.com/118258337/201899219-747cdb43-16b9-4df2-b855-94e498dd9b8f.PNG)
![11](https://user-images.githubusercontent.com/118258337/201899229-74cc8368-678e-45b2-b235-c61e198b0d8b.PNG)<br />


