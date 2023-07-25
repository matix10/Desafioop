Este archivo tiene como finalidad la instalacion y configuracion de grafana y prometheus en un servidor virtual

# Ejecucion del playbook

 ansible-playbook main.yml -i inventory.ini

 ## prometheus.yml

 Este playbook tiene se encarga de descargar el paquete de prometheus y crea el ambiente necesario (usuario, grupo y directorios) para su correcta ejecucion.

 Una vez instalado se puede visualizar las metricas en 
 http://ipservidordecontrol:9090/metricas

 
 ## grafana.yml

 Este playbook tiene se encarga de descargar el paquete de grafana y crea el ambiente necesario (usuario, grupo y directorios) para su correcta ejecucion.

  http://ipservidordecontrol/
