# RPA-TRM
Automation with RPA
INSTRUCTIONS TO RUN THE RPA DEVELOPMENT CHALLENGE
This automation aims to extract Euro and Dollar TRM information from the Banco de la República website for a specific date range. This program downloads CSV files with information of the TRM for the Euro and the Dollar. It then processes the data to obtain the averages, the highest and the lowest values of the TRM for each currency in each year, for a date range chosen by the user. Finally, it sends a report by e-mail in an Excel file.
Requirements
1.You need to have Google Chrome installed on your machine, have the browser option configured to ask for storage path every time a download is executed and set the "on open" option to "Open New Tab Page". 
2.This program does not accept work queues.
3.The following directories must be created in the path C:\Users\<UserName>\Documents\<RobotName>
*Received files: Where the files downloaded from the page will be stored.
*Base: The Config.xlsx file should be placed in this folder.
*Logs: An Excel file with the logs per day will be stored in this folder.
*Traceability: The output file that is sent by e-mail will be stored in this folder.
Assets
To run this automation in your machine the following Assets must be created in the orchestrator:


Asset Name	                         Description	                                       Value
BanrepURL		               URL para ingresar al sitio Banrep                 https://www.banrep.gov.co/estadisticas/trm
credencialCorreo		                 Credentials                Usuario: e-mail. Contraseña: e-mail's password.
RutaBase	                          Base folder	                                        Base
RutaIn	                       Folder for received files	                      Archivos Recibidos
RutaLog	                              Logs folder	                                    Logs
RutaOut	                          Traceability folder                            Trazabilidad
RutaParcialConfig	               Route for config folder     	                \TRAY\Base\Config.xlsx
RutaRaiz	                       Route for the folders	                       C:\Users\{0}\Documents\
BotName	                          Robot name                                        	TRAY

Note: Before running the program, do not forget to modify the data of your choice in the Config.xlsx file, except for the Assets tab, which does not need to be modified.
