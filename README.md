PASOS PARA CLONAR REPOSITORIO Y CLONARLO:

1. Desde la terminal, clona el repositorio en la carpeta que desees con el siguiente comando:
  git clone https://github.com/Jacobo1001/FinalTelematica.git

2. Ingresa a la carpeta donde clonaste el repositorio:
  cd "nombre_carpeta"

3. Accede a la carpeta FinalTelematica:
  cd FinalTelematica

4. Luego, entra a la carpeta FinalTelematica-Jacobo:
  cd FinalTelematica-Jacobo

5. Dentro de esta carpeta encontrarás una carpeta llamada frontend y un archivo llamado main.tf. En la carpeta frontend se encuentra todo el código de la página y su archivo Dockerfile. El archivo main.tf es el encargado de automatizar todo el proceso de creación de la máquina virtual en AWS (necesitarás credenciales) y la creación de los contenedores. Las credenciales deben estar configuradas previamente en AWS CLI.

6. Necesitarás un par de claves que crearás con el nombre "llaveIac" y de tamaño 4096 en la carpeta .ssh. Ejecuta los siguientes comandos:
  cd ~/.ssh  
  ssh-keygen -b 4096 
  chmod 400 llaveIaC 
  chmod 400 llaveIaC.pub
  cd ..  

7. Una vez dentro de la carpeta FinalTelematica-Jacobo, ejecuta el archivo main.tf con los siguientes comandos:
  cd "carpeta donde clonaste el repositorio"/FinalTelematica/FinalTelematica-Jacobo
  terraform init
  terraform fmt
  terraform validate
  terraform apply
  terraform destroy  # Si deseas destruir la infraestructura creada
