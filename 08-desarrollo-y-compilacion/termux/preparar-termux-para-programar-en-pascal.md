# PREPARAR TERMUX PARA PROGRAMAR EN PASCAL

La siguiente guía sera util para continuar con el avance académico utilizando unicamente el compilador FPC (fp-utils) de Free Pascal

## INDICE

- [Descargar Termux](#descargar-termux)
- [Actualizar](#actualizar)
- [Instalar proot-distro](#instalar-proot-distro)
- [Instalar Debian y accceder](#instalar-debian-y-acceder)
- [Configurar prompt de Debian](#configurar-prompt-de-debian)
- [Actualizar e instalar FPC (minimal)](#actualizar-e-instalar-fpc-minimal) 
- [Instalar editor de textos Nano](#instalar-editor-de-textos-nano)

### Descargar Termux

Termux es un emulador de terminal Android con un entorno Linux (sistema minimo)

    https://f-droid.org/es/packages/com.termux/


### Actualizar

Es necesario actualizar la lista para poder descargar el paquete deseado

    apt update && apt upgrade -y

> _Nota.- confirme los mensajes de los archivos nuevos_


### Instalar proot-distro

El compilador FPC no esta disponible en los repositorios de termux, para poder instalar el compilador es necesario cambiar a un sistema Linux usando la herramienta `proot-distro`, por favor instale con estos comandos:

    apt install proot-distro -y

### Instalar Debian y acceder

Descargar Debian 

    proot-distro install debian

Acceder a Debian

    proot-distro login debian

### Configurar prompt de Debian

Estos comandos permiten mejorar el prompt de Debian (root) y asi tener una mejor visualización de la terminal

    cp -r /etc/skel/.* /root/

Esta configuración sera utilizado en el proximo acceso o si desea puede ejecutar nuevamente `bash` para poder ver los cambios en el prompt


### Actualizar e instalar FPC (minimal)

Instalar FPC es muy pesado (tamaño: 200 ~ 400MB), por esta razón es recomendable utilizar el paquete de compilación `core` de la siguiente manera:

    apt update && apt install fp-utils -y

Una vez hecho estos pasos, usted podrá compilar código escrito en pascal (example.pas)

### Instalar editor de textos nano

Nano es un editor de textos CLI, es decir, no tiene interfaz gráfica, unicamente funciona por terminal, es ideal y practico usarlo en Termux, a continuación se muestra los comandos para su instalación:

    apt install nano -y

> _Nota.- Esto es opcional, usted puede instalar y usar el editor de textos que desee_