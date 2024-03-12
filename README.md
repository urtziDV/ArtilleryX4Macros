Manual de Configuración de Macros para Artillery X4 por @UrtziDV	v1.1

Descripción generada automáticamente con confianza media](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.003.png)![](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.004.png)![](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.005.png)
# Contenido
[BACKUP DE PRINTER.CFG	2](#_toc161178470)

[AÑADIR MACROS.CFG Y VARIABLES.CFG	2](#_toc161178471)

[EDITAR EL ARCHIVO PRINTER.CFG	3](#_toc161178472)

[AÑADIR LLAMADA A MACROS.CFG	4](#_toc161178473)

[ELIMINAR LOS GCODE_MACRO	4](#_toc161178474)

[AÑADIR SCREW_TILT_ADJUST	5](#_toc161178475)

[AÑADIR EXCLUDE_OBJECTS	6](#_toc161178476)

[AÑADIR GCODE_ARCS	6](#_toc161178477)

[CORREGIR EL CENTRADO DE LA CAMA	7](#_toc161178478)

[ACTIVAR WEBCAM POR USB (OPCIONAL)	8](#_toc161178479)

[AJUSTAR EL ARCHIVO WEBCAM.TXT	9](#_toc161178480)

[AJUSTAR G-CODE DE LA IMPRESORA	10](#_toc161178481)

[AJUSTAR G-CODE DEL FILAMENTO	11](#_toc161178482)

[INSTALAR OCTOEVERYWHERE	12](#_toc161178483)




## <a name="_toc161160885"></a><a name="_toc161178470"></a>BACKUP DE PRINTER.CFG
Acceder a *Fluidd* a través de un navegador web, poniendo la dirección IP de la impresora y realizar una copia de seguridad del archivo **printer.cfg**

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.008.png)
## <a name="_toc161160886"></a><a name="_toc161178471"></a>AÑADIR MACROS.CFG Y VARIABLES.CFG
Desde *Fluidd* pulsar sobre el icono “+” y seleccionar Subir. Posteriormente ir a la ruta donde tengas almacenado los archivos **macros.cfg** y **variables.cfg** anteriormente descargados y selecciónalos.  ![Interfaz de usuario gráfica, Aplicación

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.011.png)

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.014.png)
## <a name="_toc161178472"></a>EDITAR EL ARCHIVO PRINTER.CFG
Acceder a *Fluidd* a través de un navegador web, poniendo la dirección IP de la impresora.  Seleccionar el archivo **printer.cfg** y pulsar sobre editar. 

### <a name="_toc161178473"></a>AÑADIR LLAMADA A MACROS.CFG
Añadir la llamada al archivo **macros.cfg** escribiendo lo siguiente:

[include macros.cfg]

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.019.png)
### <a name="_toc161178474"></a>ELIMINAR LOS GCODE\_MACRO
Eliminar todos los *[gcode\_macro]* del archivo **printer.cfg**, ya que ahora están en el **macros.cfg.** Hacer una búsqueda de gcode\_macro e ir eliminándolos hasta que indique que no hay ninguno. 

Añado un printer.cfg para usarlo de ejemplo, **NO** lo meterlo en la impresora, ya que contiene datos y ajustes únicos que solo causarían problemas en la tuya.
### <a name="_toc161178475"></a>AÑADIR SCREW\_TILT\_ADJUST
El SCREW\_TILT\_ADJUST realiza el cálculo automático para el ajuste de las ruedas de la cama en segundos. Diciéndonos cuantas vueltas y en qué sentido hay que girarlas para dejar un nivel perfecto. Por ejemplo, cuando indique 00:15 CW, significa que hay que dar un cuarto de vuelta en sentido horario.

[VIDEO DE DEMOSTRACIÓN](https://www.youtube.com/watch?v=APAbl5PGEh0&t=410s)

Los datos de los SCREW corresponden al eje X e Y. Puede que sea necesario ajustar en cada impresora con valores diferentes. El sensor de nivelación tiene que quedar centrado con el tornillo de nivelación que hay en el centro de cada rueda.

[screws\_tilt\_adjust]

screw1: 57, 18				   *# Coordenadas del centro del tornillo de nivelacion 1 alineado con el sensor de nivelacion. Ajustar cada uno en su impresora.*

screw1\_name: Tornillo Delantero Izquierdo

screw2: 228, 18                             *# Coordenadas del centro del tornillo de nivelacion 2 alineado con el sensor de nivelacion. Ajustar cada uno en su impresora.*

screw2\_name: Tornillo Delantero Derecho

screw3: 228, 190                            *# Coordenadas del centro del tornillo de nivelacion 3 alineado con el sensor de nivelacion. Ajustar cada uno en su impresora.*

screw3\_name: Tornillo Trasero Derecho

screw4: 57, 190                             *# Coordenadas del centro del tornillo de nivelacion 4 alineado con el sensor de nivelacion. Ajustar cada uno en su impresora.*

screw4\_name: Tornillo Trasero Izquierdo

horizontal\_move\_z: 10

speed: 50                                   *# Velocidad de movimiento entre ruedas de niveacion.*

screw\_thread: CW-M4                         *# Seleccionar metrica del tornillo de las ruedas de ajuste de la cama. M3=3mm / M4=4mm / M5=5mm. Ejemplo CW-M4 para metrica 4.*


Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.021.png)
### <a name="_toc161178476"></a>AÑADIR EXCLUDE\_OBJECTS
Añadiendo **EXCLUDE\_OBJECTS** permite cancelar una de las piezas durante la impresión, sin que afecte al resto. Por ejemplo, si se están imprimiendo 4 cubos, pero uno de ellos se ha despegado, permite cancelar ese y seguir con los otros 3.

[exclude\_object]    *# Habilitar exclusion de Objetos*

### <a name="_toc161178477"></a>AÑADIR GCODE\_ARCS
Editando el **GCODE\_ARCS** se consigue aumentar la resolución de las piezas reduciendo de 1 a 0.1.

[gcode\_arcs]        *# Habilitar soporte ARC* 

resolution: 0.1

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.023.png)


### <a name="_toc161178478"></a>CORREGIR EL CENTRADO DE LA CAMA
Si la cama de tu X4 está descentrada respecto al eje X, puedes corregirlo editando el apartado **[stepper x**], en este caso el valor original era -6 y se cambió a -8.

- **Tras realizar cualquier cambio en los ficheros printer.cfg o macros.cfg, es necesario SIEMPRE, reiniciar el Firmware.**

## <a name="_toc161178479"></a>ACTIVAR WEBCAM POR USB (OPCIONAL)
Si se desea poder ver el estado de la impresión desde *Fluidd* a través de una WebCam, es necesario seguir los siguientes pasos:

1. Conectar la impresora a Internet.
1. Comprobar la IP que se le ha asignado a la impresora desde la propia pantallita.
1. Desde el PC, abrir un navegador de internet, y en la barra de busqueda escribir la dirección IP de la impresora. EJ: 192.168.1.122
1. La interfaz de Fluidd de la impresora ya se debería de haber abierto.
1. En el PC, buscar el programa “cmd” o "simbolo de sistema" y pulsa botón derecho sobre el icono del programa y seleccionar ejecutar como administrador.
1. Escribir ssh mks@TUIP (EJ: ssh <mks@192.168.1.122>)

\- Usuario: mks

\- Clave: makerbase

![Texto

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.029.png)

1. Escribir: *sudo systemctl enable webcamd*
1. Escribir: *sudo systemctl start webcamd*
1. Escribir: *exit* para salir.
1. Conectar la WebCam al USB de la impresora.


### <a name="_toc161178480"></a>AJUSTAR EL ARCHIVO WEBCAM.TXT
En el archivo webcam.txt, buscar la línea que pone #camera="auto" y quitar la #. Tiene que quedar asi: camera="auto". También se puede ajustar la resolución de la imagen más abajo, con diferentes resoluciones ya preconfiguradas.


## <a name="_toc161178481"></a>AJUSTAR G-CODE DE LA IMPRESORA
Para un correcto funcionamiento, es necesario añadir el siguiente código en el Inicio y Fin de la impresión.

**G-Code de Inicio.** Editar en OrcaSlicer y poner el siguiente código:

*;Generated with Cura\_SteamEngine 4.8.0*

*G28; Hacer Home a todos los ejes.*

*START\_PRINT BED\_TEMP=[bed\_temperature\_initial\_layer\_single]*

*EXTRUDER\_TEMP=[nozzle\_temperature\_initial\_layer]*

**G-Code Final.** Editar en OrcaSlicer y poner el siguiente código:

*;G-Code Final Impresora*

*PRINT\_END*


## <a name="_toc161178482"></a>AJUSTAR G-CODE DEL FILAMENTO
Para un correcto funcionamiento, es necesario añadir el siguiente código en el Inicio y Fin de la impresión.

**G-Code de Inicio.** Editar en OrcaSlicer y poner el siguiente código:

*;G-Code Filamento*

**G-Code Final.** Editar en OrcaSlicer y poner el siguiente código:

*; Filament-specific end gcode* 

*;END gcode for filament*

Descripción generada automáticamente](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.040.png)


## <a name="_toc161178483"></a>INSTALAR OCTOEVERYWHERE
Para poder acceder a tu impresora desde cualquier parte del mundo, existe OctoEverywhere. Se puede controlar, y ver la impresión, además incluye una Inteligencia Artificial que controla mediante la cámara, en caso de tenerla instalada, el estado de la impresión y detectar si algo está yendo mal. Se puede usar en Android con OctoApp, y también se puede vincular con Telegram para que te mande notificaciones.

[ENLACE](https://octoeverywhere.com/)

![Una captura de pantalla de un celular

Descripción generada automáticamente con confianza media](Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.041.png)

Github: <https://github.com/urtziDV/ArtilleryX4Macros>	Telegram: @ArtillerySidewinderX4

[ref1]: Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.010.png
[ref2]: Aspose.Words.54234333-afda-4e5a-b7e2-edf50eb4e2de.013.png