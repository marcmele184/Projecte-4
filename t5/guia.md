
# Guia instalació SSH per linux i windows 

Per poder començar amb la instalació necesitarem les 2 maquines, una linux i una windows.

Començarem amb la guia d'instalació SSH per linux

---

# SSH linux

Un cop que hem instalat la maquina ubuntu colocarem la seguent comanda per poder actualitzar el sistema

```bash
sudo apt update && sudo apt upgrade -y 
```

**Important**

Si no hem instalat el ssh durant la instalacio de ubuntu farem la seguent comanda

```bash
sudo apt install ssh
```

Un cop que ja tenim instlat el ssh comprovarem si esta activat amb la seguent comanda

```bash
systemctl status ssh
```

Si el ssh no esta activat, el podem activar amb la seguent comanda

```bash
systemctl start ssh
```

Un cop que podem veure tal i com surt a la foto podrem seguir amb el seguent pas

![sshactivat](img/2.png)

Un cop que ja tenim instalat el ssh el seguent pas sera veure la nostre ip amb la seguent comanda

```bash
ip addr show
```
Un cop que executem aquesta comanda veurem el seguent:

![comanda per veure la ip](img/1.png)

Ara el seguent pas sera fer la conexio per ssh, en aquest cas ho farem desde una maquina windows, això ho farem amb la seguent comanda 

```bash
ssh usuari@192.168.56.101
```
Ens sortira un missatge com aquest en el qual haurem de escriure "yes" per poder continuar.

![missatge de ssh](img/3.png)

Un cop dins en demanara la contrasenya del usuari

![colocar la contrasenya](img/4.png)

Un cop que ja estem dins de la maquina el seguent pas que farem sera modificar l'arxiu de configuració, per poder editar-lo primer esc





habilitar l'usuari root

Per poder fer això neccesitarem colocar una contrasenya al root, per fer això ho escriurem amb la seguent comanda 

```bash
passwd root
```
Un cop fet aixó ens demana la contrasenya.

Quan això ja esta fet podrem inicar sessió amb el root desde ssh fent servir la seguent comanda

```bash
ssh root@192.168.56.101
```




