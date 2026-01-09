# IO_Expander
Project to create an I2C IO expander board based on available pre-made boards.

## General Specifications:
- 5V TTL 
- Greater than or equal to 96 GPIO
    - Input or output on all
- I2C
- Good documentation
    - Available Python and Arduino IDE libraries
## Primary Ideas:
PLC needs many cheap TTL remote IO. I2C GPIO boards are easy to find. The [Adafruit MCP23017](https://www.adafruit.com/product/5346) seems like a good fit. It can 8 devices on one bus so a total of 128 GPIO. A PCB can be easily created to mount all the device to and include a barrel plug for an external 5V 4A power supply. The [Sparkfun QwiicBus](https://www.sparkfun.com/sparkfun-qwiicbus-endpoint.html) is a simple device that allows extending I2C over RJ45 up to 100ft. Combining the two devices would allow for multiple modules in different locations (as long as the total doesnt go above 8). The ideal setup may be to create four 32 channel modules. This may change based on the specific cable/connector that the relay boards use. The [DFRobot GPIO Expander](https://www.dfrobot.com/product-2627.html) is another option, but needs more evaluation.

### <img src="Sparkfun_QwiicBus_EndPoint.png" alt="SparkFun QwiicBus Module" width= 50%>
### <img src="Adafruit_MCP23017_GPIO_Expander.jpeg" alt="Adafruit MCP23017 Board" width= 50%>

