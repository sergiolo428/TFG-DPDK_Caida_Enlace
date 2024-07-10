# TFG-DPDK-Caida-de-enlace
SOLUCIÓN PARA RESPUESTA ANTE FALLOS DE ENLACE EN REDES DE COMUNICACIONES

Solución DPDK basada en "link_status_interrupt" para la atención a caídas de enlace producidas en un nodo 
con el fin de realizar la activación de un enlace alternativo.

## Configuración e Instalación DPDK

Consultar la guía de instalación incluida en el repositorio

## Características Equipo

- Linux (Solo testeado en Ubuntu 23)
- NIC compatible con virtualización
- S.O. con iommu

## Compilación 

$ make

## Ejecución 

$ cd build
$ sudo ./main.c -l [Num Core] -n [Num Ram] -- -p [Port mask]

[Num Core] --> Numero de núcleos a utilizar (Debe ser igual o mayor al número de puertos)

[Num Ram] --> Numero de tarjetas de memoria 

[Port mask] --> Mascara indicando el número de puertos a utilizar --> EJ 3 puertos = 0x7
