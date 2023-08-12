# button_task

A task to turn on and off the LED using raspberry pi ,GPIOZERO 

<img src="https://th.bing.com/th/id/OIP.Bi_w22MbY-h8ImsSt0f6agAAAA?pid=ImgDet&rs=1" alt="Employee data" title="Employee Data title">

**libaries used in the code**
`
from gpiozero import Button
from gpiozero import LED
from time import sleep
`

*****Code explaining :*****
`
from gpiozero import LED, Button

button = Button(3)
led = LED(2)

clicks = 0

while True:
    # Check if button is pressed
    if button.is_pressed:
        clicks += 1
        sleep(0.5)

    # Check if number of clicks is even or odd
    if clicks % 2 != 0:
        led.on()
        sleep(0.5)

    elif clicks % 2 == 0:
        led.off()
        sleep(0.5)
`

Team:
* [Hala](@hala214)
* [Tala](@talashweiki)
        
`
