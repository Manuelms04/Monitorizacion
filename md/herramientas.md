# Monitorización de procesos

La monitorización de procesos es el seguimiento y análisis de las aplicaciones y servicios en ejecución dentro de un sistema informático para garantizar su rendimiento, estabilidad y disponibilidad. Implica observar el uso de recursos como CPU, memoria, disco y red, así como el estado de los procesos 

### *Principales objetivos:*

- Detección de problemas

- Optimización

- Seguridad

- Planeación de capacidad

---
## ps

- El comando `ps` muestra información sobre los procesos en ejecución

- Con el comando `ps aux` nos muestra informacion sobre todos los procesos de todos los usuarios, donde nos muestra mas información como el PID, estado, uso de CPU y memoria...

```bash
ps
```

```bash
ps aux
```
![](/img/herramientas/1.png)

- El comando `ps -C nano` muestra información sobre los procesos en ejecución que corresponden al programa nano
```bash
ps -C nano
```
![](/img/herramientas/2.png)

- Si deseas ver los procesos que más recursos consumen, por ejemplo, los 5 que utilizan más memoria, puedes emplear el comando `ps -eo user,pid,%cpu,%mem,time --sort=-%cpu`
```bash
ps -eo user,pid,%cpu,%mem,time --sort=-%cpu
```
![](/img/herramientas/3.png)

---

## top
- El comando `top` se utiliza para observar en tiempo real el consumo de recursos del sistema, incluyendo la CPU, la memoria y los procesos que están en ejecución
```bash
top
```
![](/img/herramientas/4.png)

- El comando `top -b -n 1 > top.txt` crea una captura de los datos de top y guarda la información en un archivo llamado ***top.txt***
```bash
top -b -n 1 > top.txt
```
![](/img/herramientas/5.png)

---

## atop
- `atop` es una herramienta avanzada de monitoreo que ofrece información detallada sobre el consumo de recursos y los procesos en ejecución
```bash
atop
```
![](/img/herramientas/6.png)

---
---

# Monitorización de procesos

La monitorización de redes consiste en el seguimiento y análisis del tráfico de datos que circula a través de una red informática. Su objetivo es garantizar que la infraestructura de red funcione de manera eficiente, segura y sin interrupciones

### *Principales objetivos:*

- Detección de problemas en la red y problemas de conectividad

- Mejorar el rendimiento de la red mediante el análisis del tráfico 

- Detectar intrusiones, ataques o actividades sospechosas para proteger la red

- Asegurar que la red esté preparada para soportar el crecimiento del tráfico

---

## TCPDUMP

- El comando `tcpdump` es una herramienta de línea de comandos que facilita la captura y el análisis de paquetes de red en un sistema. Es especialmente útil para solucionar problemas de red, examinar el tráfico y realizar tareas de seguridad
```bash
tcpdump
```
![](/img/herramientas/7.png)

### TCPDUMP con la tarjeta de red
- Para capturar paquetes de red con `tcpdump`, es necesario indicar la interfaz de red que deseas monitorear. Puedes ver las interfaces de red disponibles en tu sistema utilizando los comandos ip a o ifconfig

```bash
tcpdump -i 'nombre de la tarjeta'
```
![](/img/herramientas/8.png)

### TCPDUMP redireccionando a un archivo
- Para guardar la salida de `tcpdump` en un archivo, puedes redirigir la salida a un archivo de texto utilizando el operador `>`

#### ***Pasos a seguir:***
```bash
tcpdump -i 'nombre de la tarjeta' -w 'nombre del archivo'
```
```bash
chown root:root 'nombre del archivo'
```
```bash
tcpdump -r 'nombre del arhivo' > 'nombre del nuevo archivo .txt'
```
```bash
cat 'nombre del nuevo archivo .txt'
```
![](/img/herramientas/9.png)
![](/img/herramientas/10.png)

---

## TCPTRACK
- `tcptrack` es una herramienta de línea de comandos que muestra el tráfico de red en tiempo real. Proporciona información sobre las conexiones TCP activas en un sistema, incluyendo las direcciones IP, los puertos y el estado de cada conexión
```bash
tcptrack
```
![](/img/herramientas/11.png)

---

## IPTRAF
- `iptraf` es una herramienta de monitoreo de red en tiempo real para sistemas Linux, creada para ofrecer estadísticas detalladas sobre el tráfico de red.
```bash
iptraf
```
![](/img/herramientas/12.png)
![](/img/herramientas/13.png)

---

## BMON
- Bandwidth Monitor, `BMON` es una herramienta de monitoreo en Linux que se utiliza para supervisar el ancho de banda y el tráfico de red en tiempo real
```bash
bmon
``` 
![](/img/herramientas/14.png)

---
---

# Monitorización de almacenamiento

![](/img/herramientas/15.png)
![](/img/herramientas/16.png)
![](/img/herramientas/17.png)
![](/img/herramientas/18.png)
![](/img/herramientas/19.png)

