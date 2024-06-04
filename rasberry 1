from machine import Pin
import time

led1 = Pin(15, Pin.OUT)                  # LED 1 on GP15
led2 = Pin(17, Pin.OUT)                  # LED 2 on GP17
button1 = Pin(13, Pin.IN, Pin.PULL_UP)   # Button 1 on GP13
button2 = Pin(14, Pin.IN, Pin.PULL_UP)   # Button 2 on GP14
button3 = Pin(16, Pin.IN, Pin.PULL_UP)   # Button 3 on GP16

try:
    while True:
        if not button1.value() or not button2.value():
            led1.value(1)  # Turn on LED 1
        else:
            led1.value(0)  # Turn off LED 1
        
        if not button3.value():
            led2.value(1)  # Turn on LED 2
        else:
            led2.value(0)  # Turn off LED 2
        
        time.sleep(0.1)  # Small delay to debounce buttons
except:
    pass
