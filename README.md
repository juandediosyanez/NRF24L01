# NRF24L01
Módulo Python que permite el control de un módulo de radio Arduino tipo NRF24L01.

**Nota1:** *este repositorio tiene como finalidad ayudar a aquellas personas que quieran utilizar un módulo de radio en sus proyectos maker. Aglutinando y puliendo partes del trabajo de otros profesionales para hacer posible su uso de forma más sencilla (y en Español).*

Dicho esto, este pequeño módulo esta diseñado para ser utilizado con una SBC tipo Raspberry u otro modelo siempre que contenga un bus GPIO y pueda correr las dependencias **py-spidev**. Concretamente este módulo se ha probado en una Raspberry PI 3B.

Dentro de los archivos se podrá encontrar una copia de **py-spidev** como del módulo **NRF24L01** y a continuación una explicación de como instalarlos.

## Clona el repositorio en tu Raspberry ##

```
mkdir NRF24L01
cd NRF24L01/
git clone https://github.com/juandediosyanez/NRF24L01
```

## Instalación de py-spidev ##

Estas dependencias nos permitirán que cuando conectemos nuestro módulo NRF24L01 al bus GPIO de nuestra Raspberry, esta pueda reconocerlo. Estas dependencias se pueden encontrar originalmente en https://github.com/Gadgetoid/py-spidev/. Para instalarlas abriremos la terminal y procederemos a:

```
cd py-spidev/
unzip py-spidev-master.zip
rm py-spidev-master.zip

cd py-spidev-master

# Python2 o Python3
sudo python setup.py install  # python2
sudo python3 setup.py install  # python3
```

## Acceder al módulo NRF24L01 ##

Como todo módulo solo tenemos que añadirlo a nuestro proyecto y hacerle referencia como si se tratase de una función. Para localizarlo, junto a algunos ejemplos, podemos encontrarlo con el nombre de **nrf21l01.py** en:

```
  NRF24L01
  │   LICENSE
  │   README.md    
  │
  └───NRF24L01
  │   │   nrf24l01.py <----- ¡AQUÍ!
  │   │
  │   └───ejemplos
  │       │   ejemplo_nrf24l01-emisor.py
  │       │   ejemplo_nrf24l01-receptor.py
  │       │   ...
  │   
  └───py-spidev
      │   py-spidev-master.rar
```

Localizado ya podemos copiarlo y trabajar con él. Para conocer cómo funciona lo suyo es entrar en **ejemplos** y leerlos detenidamente, ver los comentarios (en inglés) y echarle algo de lógica al tema. Los ejemplos dejados son para trabajar con el módulo y la **biblioteca RPi.GPIO** de nuestra Raspberry PI.

***Nota2:** se agradecería en caso de usar este módulo en alguno de sus proyectos, que en la publicación de los mismos se hiciese mención de este repositorio. Y si lo deseas puedes seguirme en mi Twitter o Instagram -> @juandediosyanez*

![Problemas al cargar la imagen](https://github.com/juandediosyanez/NRF24L01/blob/master/NRF24L01/conexiones.jpg)

**Referencias ->** [Spidev de Gadgetoid](https://github.com/Gadgetoid/py-spidev/) | [lib_nrf24 de Blavery](https://github.com/BLavery/lib_nrf24)
