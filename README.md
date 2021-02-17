# RPA-TRM
Automatización con RPA \n
INSTRUCCIONES PARA CORRER EL RETO DE DESARROLLO RPA \n
Esta automatización tiene como objetivo extraer información de la TRM del Euro y del Dólar de la página del Banco de la República para un rango de fechas específico. Este programa descarga archivos CSV con información de la TRM para el Euro y el Dólar. Posteriormente procesa los datos para obtener los promedios, el valor mayor y el valor menor de la TRM para cada moneda en cada año, para un rango de fechas escogido por el usuario. Finalmente envía un reporte por correo electrónico en un archivo de Excel. \n
Requerimientos
1.Necesita tener instalado Google Chrome en su máquina, tener configurada la opción del explorador para preguntar ruta de almacenamiento cada vez que se ejecuta una descarga y configurar la opción “al abrir” con “Abrir la página Nueva Pestaña”. 
2.Este programa no acepta colas de trabajo.
3.Se deben crear en la ruta C:\Users\<NombreUsuario>\Documents\<nombreRobot> los siguientes directorios:
*Archivos recibidos: Donde se almacenarán los archivos descargados de la página.
*Base: En esta carpeta se debe ubicar el archivo Config.xlsx
*Logs: Se almacenará un archivo en Excel con los logs por día.
*Trazabilidad: Se almacenará el archivo de salida que es enviado por correo electrónico.
Assets
Para correr esta automatización en su máquina se deben crear los siguientes Assets en el orquestador:


Nombre Asset	                         Descripción	                                       Valor
BanrepURL		               URL para ingresar al sitio Banrep                 https://www.banrep.gov.co/estadisticas/trm
credencialCorreo		Credenciales para enviar reporte                Usuario: Su correo deseado. Contraseña: La contraseña del correo.
RutaBase	                    Nombre carpeta base	                                        Base
RutaIn	                       Nombre carpeta archivos recibidos	                  Archivos Recibidos
RutaLog	                          Nombre carpeta Logs	                                    Logs
RutaOut	                      Nombre carpeta trazabilidad	                            Trazabilidad
RutaParcialConfig	     Ruta especificada para acceder a la carpeta config      	\TRAY\Base\Config.xlsx
RutaRaiz	                     Ruta base para las carpetas	                       C:\Users\{0}\Documents\
BotName	                          Nombre del Robot                                        	TRAY

Nota: Antes de correr el programa no olvide modificar los datos de su preferencia del archivo Config.xlsx, a excepción de la pestaña Assets, la cual no es necesaria modificar.
