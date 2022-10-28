# LRRAAJLS-Raspberry-Team

# Sistemas programables

## 37 Sensor KIT



## Joystick
  ### Codigo
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
 
## Flame
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
## RGB LED
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
  
  
## Heartbeat
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Light cup
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Hall Magnetic
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
 
## Realy
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Linear Hall
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## SMD RGB
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Color Flash

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Tilt switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  

## 18B20 Temp

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Big Sound

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito


## Touch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Two-color

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Laser emit

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## Laser emit

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
  
## Ball switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Analog temp

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Small sound
  
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Digital temperature

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Mini two-color

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Butom 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## Photo-esistor

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## IR emission

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Tracking

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Buzzer

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
  
## Reed switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Shock

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Shock

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Ky-015 Temp 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Ky-022 IR receiver 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Avoidance 

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito

## Passive Buzzer

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
 ## Mini Switch

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
## Rotay encoders
 
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
## Analog Hall

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## Tap Module
  
  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
 
## Light blocking

  ### * Codigo
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
