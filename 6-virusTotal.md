# Metasploit y virus total
 
### Virus total
Es una plataforma que proporciona de forma gratuita el analisis de archivos y paginas web
Contiene 59 firmas antivirus, las cuales tiene como finalidad analizar y buscar contenido malicioso en cualquier archivo que se suba a la plataforma y analizar direcciones URL

Es una alternativa de escaneo de muestras online

### Modulo de post explotacion en Metasploit
Es un modulo que permite analizar muestras mediante la api de virus total pero sin que la muestra sea subida a la plataforma

Con ello podemos subirle un determinado archivo a un equipo infectado, y comprobar si al momento de ejecutar sera detectado por los antivirus

### Procedimiento 
### 1. Tener un equipo comprometido (Meterpreter)
### 2. Subirle un archivo, por ejemplo un nc.exe 

**Es un archivo disponible en kali en la ruta: /usr/share/windows-binaries**

Netcat, es una herramienta que puede ser utilizada en windows o en linus para administracion remota, se ha utilizado como un software malicioso, sin embargo no lo es

`
CON EL COMANDO: upload seguido de la ruta. El archivo se sube 
`

* upload /usr/share/windows-binaries/nc.exe C:\\Users\usuario\\Desktop

### 3. Subido el archivo, pasar Meterpreter a segundo plano y ejecutar el modulo axuliar 

* blackground
* El modulo de post explotacion se llama: "check_malware"
* search check malware
* use MODULO
* show options

Por defecto el modulo nos da la apikey de virus total, la cual nos sirve para realizar el analisis sin subir el archivo a la plataforma

**Deben configurarse los siguientes parametros:**

1. Remotefile: Archivo que sera analizado

`set REMOTEFILE C:\\Users\usuario\\Desktop\\nc.exe`


2. Session: Sesion activa de Meterpeter
   
`set SESSION 1`
   
* run

