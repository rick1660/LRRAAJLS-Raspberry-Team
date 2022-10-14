# LRRAAJLS-Raspberry-Team

# Sistemas programables

## 37 Sensor KIT



## Joystick
  ### Codigo
  
  ### Corrida
  
  ### Imagenes del circuito
  
 
 
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
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
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
  
  ### * Corrida
  
  ### * Imagenes del circuito
  
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
  
