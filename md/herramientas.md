# Monitorización:

## Monitorización de procesos

La monitorización de procesos es el seguimiento y análisis de las aplicaciones y servicios en ejecución dentro de un sistema informático para garantizar su rendimiento, estabilidad y disponibilidad. Implica observar el uso de recursos como CPU, memoria, disco y red, así como el estado de los procesos 

### *Principales objetivos:*

- Detección de problemas

- Optimización

- Seguridad

- Planeación de capacidad

---
### ps

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

### top
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

### atop
- `atop` es una herramienta avanzada de monitoreo que ofrece información detallada sobre el consumo de recursos y los procesos en ejecución
```bash
atop
```
![](/img/herramientas/6.png)















