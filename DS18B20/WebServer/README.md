In this sketch, esp8266 is uesd as a server and presenting sensor data from DS18B20 on webpage.


About hardware and wiring:

1. Thanks to oneWire system, multiple sensors could be monitored by only one GPIO interface using parallel connection.

2. Esp8266-esp-01 chip is applied here as well as a FTDI chip.

3. Wiring is simple and can be found anywhere on the internet. Just pay attention that the GPIO0 should be pulled low when
   burning the sketch into the esp8266 and pulled high when the system is functioning.
   
4. DS18B20 is easy to be burned, so a 5k ohm resistor is required when pulling up the DQ pin (pin in the middle).

5. If you fail to burn the sketch into the chip but you are pretty sure that the COM and board settings and wiring are right,
   I highly recommand you to reset the chip, check if the working voltage is 3.3V, and if there is any broken Dupont Lines and 
   then burn the sketch again.


About sketch:

1. This sketch is modified from an example sketch named AdvancedWebServer. Besides a sketch named DS18B20-With-Wifi-ESP8266 also
   gave some inspiration. Thanks to the authors.

2. You have to download OneWire.h and DallasTemperature.h to make sure the sketch run smoothly.

3. In the very end of the sketch, some unneccessary codes, which basically should function as drawing the changing temperature-time 
   graph, is reserved for you information. However I have to say that there is some undetermined bugs in that part. It will be more
   than welcome if you have the interest to help me figure it out!

4. After the system is functioning, one can type <server ip> into the address bar of a browser to view the sensor data and
    how long the system has being operating. The page is set refreshing every 5 seconds automatically. You can modify it if 
    you like.


That is almost all about it. Burn the sketch and give it a try!