# Ejercicios_finales_script_Linux

1.Escriba un script que elimine un archivo o directorio pasado como parámetro, y le pregunte si está seguro de llevar a cabo la acción.
  #!/bin/bash

#Script 1: Elimine un archivo o directorio pasado como parámetro y le pregunta si está seguro de llevar a cabo la acción

clear

if [[ -e $1 ]]; then
	if [[ -d $1 ]]; then
			read -p "¿Está seguro que quiere borrar el directorio $1? (S/N): " opcion
			if [[ $opcion == "s" || $opcion == "S" ]]; then
				rm -r $1
			fi
			
	else

			read -p "¿Está seguro que quiere borrar el fichero $1? (S/N): " opcion
			if [[ $opcion == "s" || $opcion == "S" ]]; then
				rm $1
			fi
	fi	
else
	echo "No existe el directorio o fichero introducido."
fi

2.Escribir un script que pueda mostrar información de un comando al ejecutar dicho script y pasar como parámetro el comando.
  #!/bin/bash

#Script 2: Escribir un script que pueda mostrar información de un comando al ejecutar dicho script y pasar como parámetro el comando

clear
$1 --help
  
