# MODS MACROS

Accede a nuestra comunidad de TELEGRAM: https://t.me/SorporteArtilleryX4

Todas las modificaciones han sido probadas y funcionan con OrcaSlicer v2.0.0. Se incluye entre los archivos, el perfil de OrcaSlicer (UDV) con los ajustes para la compatibilidad de las modificaciones de las macros del manual.

V1.9:
- Añadida correccion en la macro NOZZLE_WIPE. Ahora se hace un cero al extrusor antes de ejecutar el movimiento. Gracias a @Carlos_AD
  
V1.8:
- Añadidas nuevas macros EXTRUIR y RETRAER para ejecutar las ordenes del filamento desde Fluidd, por si la pantalla no funciona.
- Añadidas nuevas macros para el PID de la Cama y del Extrusor. Gracias a @Mendi107
- Corregida una errata en los comentarios de todas las macros.

V1.7:
- Generados los archivos para cada versión, X4 PLUS y X4 PRO. Ya no es necesario editar nada en los archivos, directamente introducir el de tu modelo y listo.
  
V1.6.2:
- Añadidas las posiciones para la X4 PLUS en printer.cfg. Gracias a @Tonymalone

V1.6.1:
- Añadidas las posiciones para la X4 PLUS en macros.cfg. Gracias a @Tonymalone

V1.6:
- Corrección en la macro M600 para el cambio de color.
- Eliminada la macro CARGA_LIMPIA que se usaba junto a la M600, ya no es necesaria.
- Añadida la macro M300 para activar los pitidos. Gracias a @cristobalgc10 
- Añadido pitido cuando se ejecuta la M600 para avisar del cambio de color.
- Añadido el archivo politonos.cfg con politonos para el buzzer.
	- Macro M300_MARIO con politono Super Mario Bros.
	- Macro M300_IMPERIAL con politono Star Wars - Marcha Imperial.
	- Macro M300_CARIBE con politono Piratas del Caribe.
- Corrección en plr.cfg, la macro [gcode_macro RESUME_INTERRUPTED] tenia un "gcode =" en lugar de un "gcode:". Gracias a @MisterKrujidor
- Actualizado el printer.cfg a la ultima version de Artillery, correspondiente al 19 de Marzo.
- Cambiado en el printer.cfg la velocidad al hacer home del eje Z y al realizar la malla para ganar precision.
- Añadido en el printer.cfg la configuración del buzzer para añadir pitidos. Gracias a @cristobalgc10
- Modificado el G29 para poder definir desde el Gcode Inicial, el tamaño deseado de la malla. 
	-- EJ: G29 PC4 para malla de 4x4 ... G29 PC9 para malla de 9x9.
- Ajustes en el perfil del filamento en OrcaSlicer. 
	-- Activado salto en Z automatico.
	-- Salto en z al retraerse a 0.4mm.
  
V1.5:
- Correcciones en el perfil de la impresora en OrcaSlicer. 
	-- Gcode de pausa, Gcode de cambio de filamento y Gcode cambio de capa.
	-- Textura del area imprimible.
- Correcciones en el perfil del filamento en OrcaSlicer. 
	-- Activado salto en Z normal.
	-- Salto en z al retraerse a 0.8mm.
- Correcciones en el proceso de capas de 0.2 en OrcaSlicer. 
	-- Desactivado "Reducir la retraccion del relleno" para evitar roces de la boquilla.

V1.4: (Solo actualización de Manual)
- Añadido proceso de instalar e importar perfil en OrcaSlicer.
- Explicación de como funciona la macro SCREWS_TILT_ADJUTS.
- Explicación de como funciona EXCLUDE_OBJECTS.
- Explicación de botones para encender/apagar leds del puente desde Fluidd.
  
V1.3
- Se elimina en el archivo macros.cfg la llamada al archivo variables.cfg, ya no es necesario.
- Se elimina el archivo variables.cfg, ya no es necesario.
- Se añade el archivo plr.cfg con fallo de Artillery corregido por @repuk420 
- Se añade el comando LOG_Z en la configuración del Gcode de la impresora, en "Before layer change", para almacezar la Z por si se va la luz poder reanudar.
- Cambiados los nombres de los archivos GRANTRYLED para activar y desactivar las luces del puente,
- Editada la macro M600 (pendiente de probar)
- Añadido el G28 en la macro PRINT_START y eliminado de la configuración del GCode Inicial de la Impresora,
  
v1.2:
- Añadidos archivos para el control de los leds del puente. (switchsgantryleds, switchgantryon y switchgantryoff)
- Añadido en macros.cfg el encendido automático de las luces del puente al iniciar una impresión, y apagado automático al terminar.
  
v1.1:
- Todos los [gcode macro] metidos en archivo macros.cfg
- El extrusor y la cama se calientan a la temperatura de la primera capa para la limpieza, de este modo despues de limpiar, no tiene que volver a ajustar temperaturas.
- Posicion de espera hasta calentar el extrusor a un lateral de la cama, junto a la zona de purga, para que gotee fuera y ahorrar después movimientos.
- Lineas de purgado junto al cepillo de limpieza, para ahorrar movimientos.
- Bucle de limpieza con 8 pasadas sobre el cepillo, editable en macro NOZZLE_WIPE. Sustituir el (8) por el número deseado.
- Comentarios en cada macro, explicando cada instrucción.
- En la terminal de comandos se muestra cada inicio y fin de ejecucion de las macros.
- Macro M600 para cambio de color. Gracias a @Spectrumaniaco 
- Macro M420 para cargar la malla de nivelación grabada.
- Macro para activar la tira de LEDs del puente. Gracias a @repuk420 
- Al cancelar una impresion, ahora la cama sale fuera al igual que cuando se finaliza.
- Funcion SCREW_TILT_ADJUST para calcular en formato horario, cuantas vueltas hay que darle a las ruedas de la cama para nivelarla a la perfección.
- Añadida la exclusión de objetos, para poder cancelar la impresión de una pieza pero que siga con las demás. Gracias a @miguel_amat 
- Miniatura de las piezas en Fluidd y en la pantalla de la Artillery desde OrcaSlicer.

ANTES DE NADA, HACED UNA COPIA DE SEGURIDAD DE VUESTRO PRINTER.CFG

# INSTRUCCIONES
Seguid el manual en PDF incluido.
