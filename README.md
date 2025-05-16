# aws-deploy-Angel

Deploy de instancias EC2, Auto scaling group, balanceador de carga, grupos de seguridad, etc. usando github actions y workflows.

## Antes de comenzar

Cuando se cree el repositorio, asegurarnos de crear en la configuracion de este, 2 variables secreto, que contendran el aws_access_key_id y el aws_secret_access_key, que se consiguen en la cuenta de AWS.

## Paso 1

Crear dentro de la carpeta del proyecto la carpeta .github que dentro tendra la carpeta workflows junto el archivo deploy.yml

## Paso 2

Crear el archivo template a usar en el deploy, donde se especificara los recursos a usar en la pila de CloudFormation.

## Paso 3

Hacer el llamado del template en el archivo deploy y hacer el push de los cambios. Automaticamente si todo salio bien, se empezara a ejecutar el flujo de trabajo (no es recomendable que se ejecute automaticamente como en nuestro caso). Cuando finalice nuestra pila ya estara creada en CloudFormation. 