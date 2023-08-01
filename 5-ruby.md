# Interprete de Ruby

### Que es?
Es un lenguaje de programacion reflexivo y orientado a objetos.

El lenguaje combina una sintaxis inspirada en Python y Perl, y comparte funcionalidades con ostros lenguajes como LUA

###  Consola IRB / Interprete de Ruby

El uso de IRB es parecido a Python en modo interactivo, donde se permite la inclusion de codigos linea por linea y la ejecucion de scripts Ruby.

Todo esto puede ser utilizado en Metasploit justo en el paso de post-explotacion.

Meterprter permite utilizar IRB para manupular procesos, memoria, claves del registro, filtrar exploits, etc

### Como acceder a la consola del IRB
 * Contar con una sesion de Meterpreter (Un equipo comprometido)
 * Comando : irb

**Aspecto importnate:** filtrado de exploit para cada puerto con el siguiente comando:

* framework.exploits.each_module { |n,e| x+e.new; print_good ("{e.fullname}: #{x.datastore['RPORT']}") if x.datastore['RPORT'].to_i == **445**}; nil

### Adentro del sistema
* sysinfo
* getuid
* irb
* framework.exploits.each_module { |n,e| x+e.new; print_good ("{e.fullname}: #{x.datastore['RPORT']}") if x.datastore['RPORT'].to_i == **445**}; nil
* 
