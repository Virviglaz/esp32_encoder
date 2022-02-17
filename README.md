# ESP32 rotary encoder driver

Description: This library allows you to dynamically or statically add a rotary encoder handling functionality to your project just in a few lines of code.
This driver is interrupt-driven and includes  the listed below functionality:
- Configuring the GPIO
- Noise cancellation
- Releasing the resources and deinitialization of GPIO

## Example of use (encoder is connected to pin 4 and 15)
~~~cpp
#include "esp_encoder.h"

void loop() {
  encoder enc(GPIO_NUM_4, GPIO_NUM_15);

  while (1) {
    vTaskDelay(500);
    printf("value = %d\n", enc.get_value());
  }
}
~~~
