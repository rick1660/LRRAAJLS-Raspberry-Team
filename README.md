# <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626291.png" width="946" height="144" alt="LRRAAJLS-Raspberry-Team" /></a>


 <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626292.png" width="417" height="83" alt="Sistemas programables" /></a>

 <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626293.png" width="214" height="79" alt="37 Sensor KIT" /></a>



<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626294.png" width="219" height="93" alt="Joystick" /></a>
  ~~~~
    from machine import Pin, ADC
import utime

xAxis = ADC(Pin(27))
yAxis = ADC(Pin(26))
button = Pin(17,Pin.IN, Pin.PULL_UP)

while True:
    xValue = xAxis.read_u16()
    yValue = yAxis.read_u16()
    buttonValue = button.value()
    buttonStatus = "not pressed"


    if buttonValue == 0:
        buttonStatus = "pressed"
        
        
    print("X: " + str(xValue) + ", Y: " + str(yValue) + " -- button value: " + str(buttonValue) + " button status: " + buttonStatus)
    utime.sleep(0.2)
  ~~~~
  ### Corrida
  
  ![image](https://user-images.githubusercontent.com/99373882/198747619-072d5437-fa70-4d74-a185-0aa833ccd817.png)
  
  ### Imagenes del circuito
  
 ![1666996905704](https://user-images.githubusercontent.com/99373882/198746941-beaf665b-f222-42d5-85af-254e8f9e2e9c.jpg)
 
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626295.png" width="179" height="79" alt="Flame" /></a>
Codigo
  ```from machine import Pin
import utime

flame_sensor = Pin(16, Pin.IN)
utime.sleep(2)

while True:
   if flame_sensor.value() == 1:
       print("Flame Detected")
       utime.sleep(3)
   else:
       print("No Flame")
       utime.sleep(1)
utime.sleep(0.1) 
```

  ###  Corrida
  
  ###  Imagenes del circuito
  
  
 <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626297.png" width="230" height="48" alt="RGB LED" /></a>
  ### * Codigo
   ~~~~
    #Importamos librerias
from machine import Pin,PWM
import utime
import random

#asignamos los puertos a utilizar a variables
Led_R = PWM(Pin(2))
Led_G = PWM(Pin(3))
Led_B = PWM(Pin(4))

# Definimos la frecuencia de cada pin
Led_R.freq(2000)   
Led_G.freq(2000)   
Led_B.freq(2000)   
if __name__ == "__main__":
    while True:
        # Creamos tres variables a la cual le asignamos rango de numeros aleatorios
        R=random.randint(0,65535)      
        G=random.randint(0,65535)
        B=random.randint(0,65535)
        
        #asignamos la variable con el numero aleatorio a la funcion duty de cada pin para poder controlar el ciclo de trabajo y agregar cierta cantidad de R,G o B al led
        Led_R.duty_u16(R)
        Led_G.duty_u16(G)
        Led_B.duty_u16(B)
        
        #Establecemos una pausa de 100 milisegundis
        utime.sleep_ms(100)
   ~~~~
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
   
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626301.png" width="258" height="78" alt=" Heartbeat" /></a>
  ###  Codigo
  
  ### Corrida
  
  ###  Imagenes del circuito
  
## Light cup
  ###  Codigo
  
  ###  Corrida
  
  ### * Imagenes del circuito

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626305.png" width="347" height="93" alt="Hall Magnetic" /></a>
  Codigo
 ```from machine import Pin
import utime

sensor=Pin(26, Pin.IN)
utime.sleep(1)

while True:
    if sensor.value()==1:
        print("Ningun campo detectado")
        utime.sleep(1)    
    else:
        print("Campo magnetico detectado")
        utime.sleep(1)
utime.sleep(1)
``` 
  ### * Corrida
  
  ### * Imagenes del circuito
  
 <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626306.png" width="172" height="93" alt="Realy" /></a>

   Codigo
 ```
 from machine import Pin
import utime

relay = Pin(18,Pin.OUT)

while True:
    
    relay.value(1)
    utime.sleep(0.5)
    relay.value(0)
    utime.sleep(0.5)
```
  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626307.png" width="303" height="79" alt="Linear Hall" /></a>
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626308.png" width="244" height="49" alt=" SMD RGB" /></a>
 Codigo
```
from machine import Pin
import time

led_pins = [16,17,18] # pins where RGB LED is wired
leds = [Pin(led_pins[0],Pin.OUT),Pin(led_pins[1],Pin.OUT),
        Pin(led_pins[2],Pin.OUT)] # pin control array
delay_t = 0.1 # seconds to delay between toggles
while True: # loop infinitely
    for led in leds: # loop through each led
        led.high() # led high
        time.sleep(delay_t) # wait
        led.low() # led low
        time.sleep(delay_t) # wait
 ```

  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626309.png" width="280" height="79" alt="Color Flash" /></a>

Codigo

  
  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626310.png" width="261" height="79" alt="Tilt switch" /></a>

 Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626312.png" width="295" height="90" alt="18B20 Temp" /></a>

Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626313.png" width="295" height="90" alt="Big Sound" /></a>

Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito


<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626314.png" width="149" height="73" alt="Touch" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626315.png" width="225" height="72" alt="Two-color" /></a>

Codigo
 ```
from machine import Pin
import time

led_pins = [16,17] # pins where RGB LED is wired
leds = [Pin(led_pins[0],Pin.OUT),Pin(led_pins[1],Pin.OUT)] # pin control array
delay_t = 0.1 # seconds to delay between toggles
while True: # loop infinitely
    for led in leds: # loop through each led
        led.high() # led high
        time.sleep(delay_t) # wait
        led.low() # led low
        time.sleep(delay_t) # wait
 ```
  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626319.png" width="251" height="73" alt="Ball switch" /></a>

  ### * Codigo
  ~~~
  from machine import Pin
import utime

pin=27
sensor=Pin(pin, Pin.IN)
utime.sleep(1)

while True:
    if sensor.value()==1:
        print("Sensor detectado")
        utime.sleep(2)    
    else:
        print("No detectado")
        utime.sleep(2)
utime.sleep(1)
~~~
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
##<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626320.png" width="289" height="86" alt=" Analog temp" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626321.png" width="284" height="73" alt="Small sound" /></a>
  
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Digital temperature

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626322.png" width="320" height="73" alt="Mini two-color" /></a>

  ### * Codigo
~~~
from machine import Pin
import time

led_pins = [16,17] # pins where RGB LED is wired
leds = [Pin(led_pins[0],Pin.OUT),Pin(led_pins[1],Pin.OUT)] # pin control array
delay_t = 0.1 # seconds to delay between toggles
while True: # loop infinitely
    for led in leds: # loop through each led
        led.high() # led high
        time.sleep(delay_t) # wait
        led.low() # led low
       time.sleep(delay_t) # wait
~~~

  ### * Corrida
  
  ### * Imagenes del circuito
  
<a href="https://cooltext.com"><img src="https://images.cooltext.com/5626323.png" width="146" height="46" alt="Butom " /></a>

  ### * Codigo
  ~~~
from machine import Pin
from time import sleep

led = Pin(14, Pin.OUT)    # 14 number in is Output
push_button = Pin(13, Pin.IN)  # 13 number pin is input

while True:
  
  logic_state = push_button.value()
  if logic_state == True:     # if push_button pressed
      led.value(1)             # led will turn ON
  else:                       # if push_button not pressed
      led.value(0)             # led will turn OFF
  ~~~~  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626324.png" width="284" height="73" alt="Photo-esistor" /></a>
  ### * Codigo
~~~~
  from machine import Pin
import time
 
ldr = machine.ADC(27)
 
while True:
     print(ldr.read_u16())
     time.sleep(0.5)
 ~~~~
 
  ### * Corrida
  
  ### * Imagenes del circuito

## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626325.png" width="278" height="73" alt="IR emission" /></a>

  ### * Codigo
  ~~~
  
import machine
from ir_tx import NEC
import utime

sensorIR = machine.Pin(26, machine.Pin.OUT) #ADC0 sera mi salida de datos analogicos
sensorIR.value(0)# asignamos valor
nec = NEC(sensorIR)
sw = machine.Pin(0,machine.Pin.IN)

while True:
    if sw.value() == 0:
        nec.transmit(0x0000, 0x09) #trasfiero este valor
    machine.sleep_ms(100)
~~~
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626326.png" width="210" height="86" alt="Tracking" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626327.png" width="178" height="81" alt="Buzzer" /></a>

  ### * Codigo
  ~~~~
    from machine import Pin, PWM
from time import sleep

buzzerPIN=16
BuzzerObj = PWM(Pin(buzzerPIN))

def buzzer(buzzerPinObject,frequency,sound_duration,silence_duration):

    # Set duty cycle to a positive value to emit sound from buzzer
    buzzerPinObject.duty_u16(int(65536*0.1))
    # Set frequency
    buzzerPinObject.freq(frequency)
    # wait for sound duration
    sleep(sound_duration)
    # Set duty cycle to zero to stop sound
    buzzerPinObject.duty_u16(int(65536*0))
    # Wait for sound interrumption, if needed 
    sleep(silence_duration)


#set translation table from note to frequency
do5=523
dod5=554
re5=587
red5=622
mi5=659
fa5=698
fad5=739
sol5=784
sold5=830
la5=880
lad5=932
si5=987


buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,la5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,sold5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,do5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,la5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.5,0.1)

buzzer(BuzzerObj,sol5,0.1,0.1)
buzzer(BuzzerObj,fa5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,re5,0.5,0.1)

buzzer(BuzzerObj,fa5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,red5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,re5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,la5,0.1,0.1)
buzzer(BuzzerObj,si5,0.5,0.1)

buzzer(BuzzerObj,mi5,0.1,0.1)
buzzer(BuzzerObj,do5,0.1,0.1)
buzzer(BuzzerObj,si5,0.1,0.1)
buzzer(BuzzerObj,la5,0.5,0.1)

#Deactivates the buzzer
BuzzerObj.deinit()
  ~~~~
  
  ### * Corrida
  ![image](https://user-images.githubusercontent.com/99373882/198747542-c0625f35-d8f5-48d0-bfd4-aeab13b235b9.png)
  
  ### * Imagenes del circuito
  ![1666996945350](https://user-images.githubusercontent.com/99373882/198746959-51e16cb4-1565-448f-a856-c2176ba11dd9.jpg)
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626328.png" width="259" height="73" alt="Reed switch" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626330.png" width="231" height="108" alt="White" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626331.png" width="286" height="85" alt="Ky-015 Temp " /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626332.png" width="406" height="85" alt="Ky-022 IR receiver " /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626333.png" width="239" height="73" alt="Avoidance " /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626334.png" width="327" height="81" alt="Passive Buzzer" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
 ## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626335.png" width="271" height="73" alt="Mini Switch" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626337.png" width="326" height="85" alt="Rotay encoders" /></a>
 
  ### * Codigo
  ~~~~
  import board
import digitalio

dirPin = digitalio.DigitalInOut(board.GP16)
stePin = digitalio.DigitalInOut(board.GP17)
dirPin.direction  = digitalio.Direction.INPUT
stepPin.direction = digitalio.Direction.INPUT

dirPin.pull = digitalio.Pull.UP
stepPin.pull = digitalio.Pull.UP
previousValue = True
while 1==1:
    if previousValue != stepPin.value:
        if stepPin.value == False:
            if dirPin.value == False:
                print("A la izquierda, a al izquierda!")
            else:
                print("A la derecha,a la derecha")
        previousValue = stepPin.value
  ~~~~
  ### * Corrida
  ![Screenshot_3](https://user-images.githubusercontent.com/99373882/196571975-12001837-7a48-4c41-82c6-1bd397529fd1.png)
  ### * Imagenes del circuito
  ![1666996945345](https://user-images.githubusercontent.com/99373882/198746987-61b90273-c06c-47cf-b874-0903dafa58f2.jpg)
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626338.png" width="281" height="86" alt="Analog Hall" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626339.png" width="228" height="55" alt="Tap Module" /></a>
  
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## <a href="https://cooltext.com"><img src="https://images.cooltext.com/5626340.png" width="311" height="86" alt="Light blocking" /></a>

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
