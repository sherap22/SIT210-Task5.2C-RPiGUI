from tkinter import *
import tkinter.font
from gpiozero import LED
import RPi.GPIO
RPi.GPIO.setmode(RPi.GPIO.BCM)

# Hardware #

led_red = LED(26)
led_brown = LED(19)
led_grey = LED(20)

## GUI DEFINITIONS
win1 = Tk()
win1.title("LED_RED toggler")
myFont = tkinter.font.Font(family = 'Arial', size = 12, weight = 'bold')




## EVENT FUNCTION ##
def ledToggle1():
    if led_red.is_lit:
        led_red.off()
        ledButton1["text"] = "Turn RED-LED ON"
        
    else:
        led_red.on()
        ledButton1["text"] = "Turn RED-LED OFF"
        
def ledToggle2():
    if led_brown.is_lit:
        led_brown.off()
        ledButton2["text"] = "Turn BROWN-LED ON"
        
    else:
        led_brown.on()
        ledButton2["text"] = "Turn BROWN-LED OFF"
        
def ledToggle3():        
    if led_grey.is_lit:
        led_grey.off()
        ledButton3["text"] = "Turn GREY-LED ON"
        
    else:
        led_grey.on()
        ledButton3["text"] = "Turn GREY-LED OFF"
        
def close():
    RPi.GPIO.cleanup()
    win1.destroy()


### WIDGETS ###
ledButton1 = Button(win1, text = 'Turn RED-LED ON', font = myFont, command = ledToggle1, bg = 'red', height = 1, width = 24)
ledButton1.grid(row=1,column=0)

ledButton2 = Button(win1, text = 'Turn BROWN-LED ON', font = myFont, command = ledToggle2, bg = 'brown', height = 1, width = 24)
ledButton2.grid(row=2,column=0)

ledButton3 = Button(win1, text = 'Turn GREY-LED ON', font = myFont, command = ledToggle3, bg = 'grey', height = 1, width = 24)
ledButton3.grid(row=3,column=0)

exitButton = Button(win1, text = 'EXIT', font = myFont, command = close, bg = 'yellow', height = 1, width = 24)
exitButton.grid(row=4,column=0)
