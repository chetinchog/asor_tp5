# Trabajo Practivo Nº5
## Networking

- [Interfaces](https://github.com/gedera/asor/blob/master/tp5_template.md#interfaces)
- [ARP](https://github.com/gedera/asor/blob/master/tp5_template.md#arp)
- [Rutas](https://github.com/gedera/asor/blob/master/tp5_template.md#rutas)

### Interfaces
1. Cómo puede determinar las interfaces de red que detectó el hardware de su máquina?
2. Configure la interfaz `enp1s0` con la dirección `172.16.0.XXX/24`. Que es el `/24` o `255.255.255.0`?. Qué uso e importancia tiene?
3. Modifique los archivos correspondientes para que la interfaz mantenga permanentemente la dirección cada vez que se reinicie.
4. Cómo verificar que ip tiene asignada en el momento.
5. Cómo eliminar una ip asignada.
6. Cómo deshabilitar el servicio de networking? Cómo deshabilitar solo la interface `enp1s0`?
7. Investigue la funcionalidad del comando `ipcalc` y realice un ejemplo utilizando el mismo.
8. Investigue la funcionalidad del comando `ping` y realice un ejemplo utilizando el mismo.
### ARP
1. Investigue para qué sirve **Address Resolution Protocol (ARP)**.
2. Para qué sirve el comando `ip neighbor`. Explique el resultado de ejecutar el comando `ip neighbor show`.
3. Amarre la ip `192.168.50.20` a la mac-address `1c:6f:65:c1:84:e2` via la interfza `enp1s0` en la tabla **ARP**.
4. Cambie la entrada de mac `1c:6f:65:c1:84:e2` por `1c:6f:65:c1:84:e5`.
5. Elimine el amarre realizado en el ejercicio anterior.
6. Como elimina todas las entradas de la tabla **ARP**.
7. Investigue la funcionalidad del comando `arping` y realice un ejemplo utilizando el mismo.
### Rutas
1. Para qué sirve el comando `ip route`?. Analice la siguiente salida
> apt-get install arping
```bash
default via 192.168.20.1 dev enp1s0 proto dhcp                                   metric 100 
192.168.160.0/24         dev enp1s1 proto kernel scope link src 192.168.160.130  metric 1
192.168.20.0/24          dev enp1s0 proto kernel scope link src 192.168.20.214   metric 100
```
2. Para qué sirve el comando `route -n`?. Analice el siguiente resultado explicando el mismo.



|   Destination |      Gateway |       Genmask | Flags   |   Metric |   Ref |   Use | Iface   |
| :-----------: |    :-------: | :-----------: | :-----: | :------: | :---: | :---: | :-----: |
|  192.168.20.0 |      0.0.0.0 | 255.255.255.0 | U       |        0 |     0 |     0 | enp1s0  |
| 192.168.160.0 |      0.0.0.0 | 255.255.255.0 | U       |        0 |     0 |     0 | enp1s1  |
|       0.0.0.0 | 192.168.20.1 |       0.0.0.0 | UG      |        0 |     0 |     0 | enp1s0  |



3. Cómo asigna una ruta por defecto.
4. Cómo cambia la ruta por defecto.
5. Cómo se habilita el routing en linux (/proc/sys)?. Para qué sirve?
6. Investigue qué diferencia existe en el ruteo estático y el ruteo dinámico.
7. Estudie la utilidad `traceroute` y `mtr`.  Para que las puede utilizar ? Cual brinda más información?
8. Estudie para que sirven los comandos `iftop`, `bmon`.
9. Estudie para que sirve el comando `tcpdump`

