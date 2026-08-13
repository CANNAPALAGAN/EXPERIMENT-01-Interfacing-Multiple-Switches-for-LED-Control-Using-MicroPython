# EXPERIMENT-01-Interfacing-Multiple-Switches-for-LED-Control-Using-MicroPython


 
## NAME:

## DEPARTMENT:

## ROLL NO:

## DATE OF EXPERIMENT:

## AIM

To interface multiple switches with the Raspberry Pi Pico and control LEDs using MicroPython.

## APPARATUS REQUIRED

1. Raspberry Pi Pico - 1

2. Push Button Switches - 2

3. LEDs (Light Emitting Diodes) -3

4. Buzzer - 1

5. 330Ω Resistors -3

6. Breadboard

7. Jumper Wires

8. USB Cable

## THEORY

<img width="474" height="407" alt="image" src="https://github.com/user-attachments/assets/df0155b7-5b06-4276-aad3-0e114260605d" />

## FIGURE-01: RASPBERRY PI PICO PINOUT DIAGRAM

Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications. The Raspberry Pi Pico is a compact microcontroller board featuring a 40-pin layout, including power, ground, GPIO, and communication interface pins. It operates with a dual-core ARM Cortex-M0+ processor and supports MicroPython and C/C++ programming.

The power pins include VBUS (5V from USB), VSYS (1.8V to 5.5V input), 3V3(OUT) (regulated 3.3V output), and multiple ground (GND) connections. The board offers 26 multi-purpose GPIO pins (GP0 to GP28), which can be used for digital input, output, PWM, and communication interfaces such as I2C, SPI, and UART. It also features three analog-to-digital converter (ADC) pins (GP26, GP27, GP28), used for reading analog sensor values, along with an ADC_VREF pin to set the reference voltage.

For communication, I2C (SDA, SCL), SPI (MOSI, MISO, SCK), and UART (TX, RX) interfaces are mapped across different GPIO pins, allowing seamless connectivity with sensors and peripherals. All GPIO pins support PWM (Pulse Width Modulation), making it useful for motor control, LED brightness adjustment, and sound applications. The BOOTSEL button enables USB mass storage mode for firmware flashing, while the DEBUG pins (SWD interface) provide debugging capabilities. With its low power consumption, flexible GPIO options, and rich interface support, the Raspberry Pi Pico is widely used for IoT, embedded systems, robotics, and automation projects.

## WORKING PRINCIPLE

## Experiment 1A:
1. Connect three LEDs to any three GPIO pins configured as digital outputs. Connect the anode (positive terminal) of each LED to a GPIO pin through an appropriate current-limiting resistor, and connect the cathode (negative terminal) to the GND pin.
   
2. Connect the buzzer to any one GPIO pin configured as a digital output. Connect the positive terminal of the buzzer to the selected GPIO pin and the negative terminal to the GND pin.
   
3. Develop and execute a MicroPython program to read the switch status of the LED and control the LEDs and buzzer based on the predefined logic.


## Experiment 1B:

1. Connect the switches to the GPIO pins of the Raspberry Pi Pico configured as digital inputs. Connect pins 1.1 and 2.1 of the switches to GND, pins 1.3 and 2.3 to the 3.3 V (3V3) supply, and pins 1.2 and 2.2 to the designated GPIO input pins.

2. Connect the LEDs to the GPIO pins configured as digital outputs. Connect the anode (positive terminal) of each LED to a GPIO pin through an appropriate current-limiting resistor and connect the cathode (negative terminal) to the GND pin.

3. Develop and execute a MicroPython program to continuously monitor the states of the switches and control the corresponding LEDs according to the specified logic.

## Experiment 1C:

1. Connect the DHT22 sensor, LDR module, and potentiometer signal pins to the required GPIO pins of the controller.

2. Connect the Three LEDs (Green, Yellow, and Red) and three Relays (Motor, Fan, Light) to the designated GPIO pins, with all LED cathodes connected to GND.

3. Develop and execute the MicroPython program to read the DHT22, LDR, and potentiometer inputs and control the corresponding load LEDs through the relays.

### CIRCUIT DIAGRAM
## Experiment 1A

<img width="529" height="275" alt="image" src="https://github.com/user-attachments/assets/770f5144-8e97-4546-b657-293185fa92c9" />

## FIGURE-02:  Circuit Diagram of Digital Output Interface 

1. Connect LED 1 by connecting its anode (positive terminal) to GPIO 0 through a 330 Ω current-limiting resistor. Similarly, connect the anode of LED 2 to GPIO 2 through a 330 Ω resistor, and the anode of LED 3 to GPIO 4 through a 330 Ω resistor.

2. Connect the positive terminal of the buzzer to any one of the GPIO pins (GPIO 0, GPIO 2, or GPIO 4) configured as a digital output.

3. Connect the cathode (negative terminal) of each LED and the negative terminal of the buzzer to the GND pin of the Raspberry Pi Pico.

## Experiment 1B

<img width="829" height="439" alt="image" src="https://github.com/user-attachments/assets/f88782eb-f23f-4b65-a7a9-79c718eede2f" />


## FIGURE-03:  Circuit Diagram of Digital Input and Output Interface 


1. Connect Switch 1 by connecting pin 1.2 to GPIO 2 and Switch 2 by connecting pin 2.2 to GPIO 3 of the Raspberry Pi Pico, configuring both GPIO pins as digital inputs.

2. Connect LED 1 by connecting its anode (positive terminal) to GPIO 13 through a 330 Ω current-limiting resistor.

3. Connect LED 2 by connecting its anode (positive terminal) to GPIO 16 through a 330 Ω current-limiting resistor.

4. Connect the switch power terminals by connecting pins 1.1 and 2.1 of the switches to GND, and pins 1.3 and 2.3 to the 3.3 V (3V3) supply.

5. Connect the cathode (negative terminal) of both LEDs to the GND pin of the Raspberry Pi Pico.

## Experiment 1C (Smart Agriculture Monitoring System)

<img width="944" height="617" alt="image" src="https://github.com/user-attachments/assets/14bdae08-b5b3-4846-b3b6-0ad87d1df923" />



## FIGURE-04:  Circuit Diagram of Smart Agriculture System


1. Select the required components: three 330 Ω resistors, six LEDs, three relays, one DHT22 temperature and humidity sensor, one LDR module, and one potentiometer.
   
2. Connect the SDA (Data) pin of the DHT22 sensor to a suitable GPIO pin on the controller.
   
3. Connect the D0 pin of the LDR module to a suitable GPIO pin.
   
4. Connect the SIG pin of the potentiometer to a suitable GPIO pin.
   
5. Connect the anode (positive terminal) of the Motor load LED to a designated GPIO pin through a 330 Ω resistor.
   
6. Connect the anode (positive terminal) of the Fan load LED to a designated GPIO pin through a 330 Ω resistor.
  
7. Connect the anode (positive terminal) of the Light load LED to a designated GPIO pin through a 330 Ω resistor.
  
8. Connect the anode (positive terminal) of the Green status LED to a designated GPIO pin.
   
9. Connect the anode (positive terminal) of the Yellow status LED to a designated GPIO pin.
  
10. Connect the anode (positive terminal) of the Red status LED to a designated GPIO pin.
  
## PROGRAM (MicroPython)
''''

## Experiment 1A:

from machine import Pin
import time
print("Pi Pico")
led1 = Pin(0, Pin.OUT)
led2 = Pin(2, Pin.OUT)
led3 = Pin(4, Pin.OUT)
buzzer=Pin(4,Pin.OUT)
while True:
    led1.value(1) 
    print("LED is ON")
    time.sleep(1) 
    led1.value(0)  
    print("LED is OFF")
    time.sleep(1)
    led2.value(1) 
    print("LED is ON")
    time.sleep(1) 
    led2.value(0)  
    print("LED is OFF")
    time.sleep(1)
    led3.value(1) 
    print("LED is ON")
    time.sleep(1) 
    led3.value(0)  
    print("LED is OFF")
    time.sleep(1)
    buzzer.value(1) 
    print("Buzzer is ON")
    time.sleep(1) 
    buzzer.value(0)  
    print("Buzzer is OFF")
    time.sleep(1)




## Experiment 1B:


from machine import Pin
import time import sleep 
switch1=Pin(2,Pin.IN)
switch2=Pin(3,Pin.IN)
led1=Pin(13,Pin.OUT)
led2=Pin(16,Pin.OUT)
while True:
    sw1_state=switch1.value()
    sw2_state=switch2.value()
    print("Switch 1 State", sw1_state)
    print("Switch 2 State", sw2_state)
    led1.value(0)
    if sw1_state==1 and sw2_state==1:
        led1.value(0)
        led2.value(0)
    elif sw1_state==1:
        led1.value(1)
        sleep(0.5)
        led1.value(0)
        led2.value(0)
    elif sw2_state==1:
        led1.value(0)
        led2.value(1)
        sleep(0.5)
        led2.value(0)
    sleep(0.5)

 

## Experiment 1B:Method 2


from machine import Pin
from time import sleep
switch1=Pin(2,Pin.IN)
switch2=Pin(28,Pin.IN)
led1=Pin(13,Pin.OUT)
led2=Pin(16,Pin.OUT)
while True:
    sw1_state=switch1.value()
    sw2_state=switch2.value()
    print("Switch 1 State", sw1_state)
    print("Switch 2 State", sw2_state)
    led1.value(0)
    if sw1_state==1 and sw2_state==1:
        led1.value(0)
        print("LED1 off")
        led2.value(0)
        print("LED2 off") 
    elif sw1_state==1:
        led1.value(1)
        print("LED1 oN") 
        sleep(0.5)
        led1.value(0)
        led2.value(0)
    elif sw2_state==1:
        led1.value(0)
        led2.value(1)
        print("LED2 oN")
        sleep(0.5)
        led2.value(0)
    sleep(0.5)


 
## Experiment 1C:


from machine import Pin, ADC
import dht
import time
# =========================
# SENSOR SETUP
# =========================

# DHT22
dht_sensor = dht.DHT22(Pin(28))

# Soil moisture simulation
soil_sensor = ADC(26)

# LDR module
ldr = Pin(27, Pin.IN)

# =========================
# RELAYS
# =========================

pump = Pin(3, Pin.OUT)
fan = Pin(4, Pin.OUT)
light = Pin(5, Pin.OUT)

# =========================
# LED STATUS
# =========================

green_led = Pin(2, Pin.OUT)
yellow_led = Pin(1, Pin.OUT)
red_led = Pin(0, Pin.OUT)

print("==============================")
print("SMART AGRICULTURE SYSTEM")
print("==============================")

while True:

    # =========================
    # READ SOIL MOISTURE
    # =========================

    soil_value = soil_sensor.read_u16()

    print("Soil Moisture:", soil_value)

    # Dry soil
    if soil_value < 20000:
        pump.value(1)
        green_led.value(1)
        print("Dry Soil -> Pump ON")

    else:
        pump.value(0)
        green_led.value(0)
        print("Soil OK -> Pump OFF")

    # =========================
    # READ DHT22
    # =========================

    dht_sensor.measure()

    temp = dht_sensor.temperature()
    humidity = dht_sensor.humidity()

    print("Temperature:", temp)
    print("Humidity:", humidity)

    # High temperature
    if temp > 35:
        fan.value(1)
        red_led.value(1)
        print("High Temp -> Fan ON")

    else:
        fan.value(0)
        red_led.value(0)
        print("Low Temp -> Fan OFF")

    # =========================
    # READ LIGHT SENSOR
    # =========================

    light_state = ldr.value()

    # Dark condition
    if light_state == 0:
        light.value(1)
        yellow_led.value(1)
        print("Dark -> Grow Light ON")

    else:
        light.value(0)
        yellow_led.value(0)
        print("Bright -> Grow Light OFF")

    print("---------------------------")

    time.sleep(2)


 
## OUTPUT


## Experiment 1A:



## FIGURE-05: CIRCUIT CONNECTION



## FIGURE-06: CODE EXECUTION OUTPUT



## FIGURE-07: LED AND BUZZER STATUS


## Experiment 1B:


## FIGURE-08: CIRCUIT CONNECTION



## FIGURE-09: CODE EXECUTION OUTPUT



## FIGURE-10: LED STATUS BASED ON SWITCH INPUTS


## FIGURE-11: LED AND GATE STATUS


## Experiment 1C:


## FIGURE-12: CIRCUIT CONNECTION (WITHOUT APPLYING ANY INPUT)



## FIGURE-13: WHEN TEMPERATURE AND HUMIDITY IS HIGH FAN (RED LED) ON



## FIGURE-14: WHEN TEMPERATURE AND HUMIDITY IS LOW FAN (RED LED) OFF



## FIGURE-15: WHEN LIGHT INTENSITY IS LOW LIGHT (YELLOW LED) OFF



## FIGURE-16: WHEN LIGHT INTENSITY IS HIGH LIGHT (YELLOW LED) ON



## FIGURE-17: WHEN MOISTURE LEVEL IS LOW IN POTENTIOMETER THEN MOTOR (GREEN LED) ON



## FIGURE-18: WHEN MOISTURE LEVEL IS HIGH IN POTENTIOMETER THEN MOTOR (GREEN LED) OFF


## RESULTS

The multiple switches connected to the Raspberry Pi Pico successfully controlled the LEDs based on their states, confirming the proper interfacing of digital inputs and outputs.

