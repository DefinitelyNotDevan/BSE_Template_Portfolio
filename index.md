# IOT Weather Indicator
I am working an IOT Weather Indicator. This project will grab weather from the internet using API's and will display them on a small screen.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Devan G | Mark Day School | Electrical Engineering | Incoming 7th Grader

TBD
  
# Final Milestone

My final milestone was coding animations for my OLED display so my IOT Weather Indicator can have more personality. I also added some text that would say what the weather was like cloudy, clear, rain, etc. I had to deserialize an array to get access to the descriptions of the weather and also in that array are something called icons. Those icons won't actually display on my screen but I used them to display animations. After I had deserialized everything, I then added an if statement saying that if this icon = true, display this animation. Now, my display has animations that make my project more alive.
~~~arduino
void sunny() {
  display.setTextSize(1);
  display.setTextColor(SH110X_WHITE);
  display.fillCircle(1, 1, 14, SH110X_WHITE);
  display.drawLine(18, 2, 40, 2, SH110X_WHITE);
  display.drawLine(15, 10, 36, 18, SH110X_WHITE);
  display.drawLine(8, 17, 22, 36, SH110X_WHITE);
  display.drawLine(2, 22, 2, 44, SH110X_WHITE);
  display.display();
  delay(1000);
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SH110X_WHITE);
  display.setCursor(92, 10);
  display.println(temp);
  display.setCursor(92, 42);
  display.println(description);
  display.drawLine(86, 0, 86, 64, SH110X_WHITE);
  display.fillCircle(1, 1, 14, SH110X_WHITE);
  display.drawLine(29, 2, 51, 2, SH110X_WHITE);
  display.drawLine(26, 14, 47, 22, SH110X_WHITE);
  display.drawLine(15, 27, 29, 46, SH110X_WHITE);
  display.drawLine(2, 33, 2, 55, SH110X_WHITE);
  display.display();
  delay(1000);
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SH110X_WHITE);
  display.setCursor(92, 10);
  display.println(temp);
  display.setCursor(92, 42);
  display.println(description);
  display.drawLine(86, 0, 86, 64, SH110X_WHITE);
  display.fillCircle(1, 1, 14, SH110X_WHITE);
  display.drawLine(40, 2, 62, 2, SH110X_WHITE);
  display.drawLine(37, 18, 58, 26, SH110X_WHITE);
  display.drawLine(23, 37, 36, 56, SH110X_WHITE);
  display.drawLine(2, 44, 2, 66, SH110X_WHITE);
  display.display();
  delay(1000);
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SH110X_WHITE);
  display.setCursor(92, 10);
  display.println(temp);
  display.setCursor(92, 42);
  display.println(description);
  display.drawLine(86, 0, 86, 64, SH110X_WHITE);
  display.fillCircle(1, 1, 14, SH110X_WHITE);
  display.drawLine(51, 2, 73, 2, SH110X_WHITE);
  display.drawLine(48, 22, 69, 30, SH110X_WHITE);
  display.drawLine(32, 51, 38, 66, SH110X_WHITE);
  display.drawLine(2, 55, 2, 77, SH110X_WHITE);
  display.display();
  delay(1000);
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SH110X_WHITE);
  display.setCursor(92, 10);
  display.println(temp);
  display.setCursor(92, 42);
  display.println(description);
  display.drawLine(86, 0, 86, 64, SH110X_WHITE);
  display.fillCircle(1, 1, 14, SH110X_WHITE);
  display.drawLine(62, 2, 85, 2, SH110X_WHITE);
  display.drawLine(59, 26, 80, 34, SH110X_WHITE);
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SH110X_WHITE);
  display.setCursor(92, 10);
  display.println(temp);
  display.setCursor(92, 42);
  display.println(description);
  display.drawLine(86, 0, 86, 64, SH110X_WHITE);
  display.fillCircle(1, 1, 14, SH110X_WHITE);
  display.display();
  delay(1000);



}
~~~
This is the sun animation!
<iframe src="https://giphy.com/embed/R4HIujv7tfpPSTIEbb" width="480" height="443" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/R4HIujv7tfpPSTIEbb"></a></p>

[![Final Milestone](https://res.cloudinary.com/marcomontalbano/image/upload/v1626814674/video_to_markdown/images/youtube--Hz94wXyT_y8-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=Hz94wXyT_y8&ab_channel=BlueStampEng "Final Milestone"){:target="_blank" rel="noopener"}

# Second Milestone

My second milestone was coding my OLED display to display the weather. First I had to solder some pins to my OLED display because otherwise, my display has no way to connect to my ESP32. After I soldered some pins into my OLED display, I then installed the libraries in Arduino IDE that would allow me to actually display things on my OLED. The original library I installed was really buggy and didn't work. Later, I installed a different library that worked perfectly. I then played around with my [display](https://randomnerdtutorials.com/esp32-ssd1306-oled-display-arduino-ide/). One note is that the libraries that actually works is called Adafruit SH110X.
```arduino
   display.setTextSize(1);
   display.setTextColor(SH110X_WHITE);
   display.setCursor(92, 10);
   display.println(temp);
   display.display();
   ```
This is the code that displays the temperature!
![IMG-0425](https://user-images.githubusercontent.com/87206622/126001342-f335b66d-3077-40e8-816e-8855ffcf80a4.jpg)

[![Second Milestone](https://res.cloudinary.com/marcomontalbano/image/upload/v1626463700/video_to_markdown/images/youtube---DjdSz2TALM-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=-DjdSz2TALM&ab_channel=BlueStampEng "Milestone 2"){:target="_blank" rel="noopener"}
# First Milestone
 

My first milestone was coding a script in Arduino that would allow my ESP32 to connect to the wifi, grab API's off the internet, and then give me the temperature. First up was connecting my ESP32. All I did was plug a micro-usb charger into my computer and then I connected the charger to my ESP32. Next I downloaded the ESP32 Drivers and the Arduino application. I then watched a tutorial on how to connect an ESP32 board to the Arduino app. [Connecting ESP32 Website](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/). Then, I connected my ESP32 to wifi using this video. [Connecting ESP32 to Wifi](https://www.youtube.com/watch?v=klIBePOzXpo&ab_channel=Techtutorialsx). After connecting my ESP32 to wifi, I then got my API's from this website. [Weather Api's](https://openweathermap.org/api). Then used a get request to get those API's. [Get Request](https://www.youtube.com/watch?v=s_2cw0k6lgs&t=11s&ab_channel=Techtutorialsx). After I got the API's I had to deserialize it and make it legible following this tutorial. [Deserialize](https://www.youtube.com/watch?v=nfr6wddRRxo&ab_channel=BenoitBlanchon). Now my code gets the weather and it is really accurate.![Screenshot (17)](https://user-images.githubusercontent.com/87206622/126001977-f95c9f75-5e13-4128-adfd-359cc691a88c.png)

```arduino
      if (err) {
        Serial.print("ERROR: ");
        Serial.println(err.c_str());
        return;
      }
      String mainString = doc["main"].as<String>();

      DynamicJsonDocument main (2048);

      DeserializationError err2 = deserializeJson(main, mainString);

      if (err2) {
        Serial.print("ERROR: ");
        Serial.println(err2.c_str());
        return;
      }

      temp = main["temp"].as<double>();
      temp = round((temp - 273.15) * 9 / 5 + 32);
      Serial.println(temp);
```
This is the code that deserializes the temperature!
![Screenshot (17)](https://user-images.githubusercontent.com/87206622/126002001-6d9d72d1-4853-4773-8154-82a4a6edb489.png)

[![First Milestone](https://res.cloudinary.com/marcomontalbano/image/upload/v1625860918/video_to_markdown/images/youtube--5ZMQx948rd4-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=5ZMQx948rd4&ab_channel=BlueStampEng "First Milestone"){:target="_blank" rel="noopener"}
