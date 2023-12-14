![FING - UDELAR](https://www.fing.edu.uy/sites/default/files/2022-06/Logo_Fing%2BUdelar_horizontal_RGB.jpg)

![kubernetes](https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Kubernetes_logo_without_workmark.svg/247px-Kubernetes_logo_without_workmark.svg.png) ![HELM](https://helm.sh/img/helm.svg)


# kubernetesFingProject

Proyecto de fin de curso kubernetes - Facultad de Ingeniería - UdelarR

Este proyecto genera un chart helm, el cual hace un despliege automático 
de una aplicación en tres capas en kubernetes.


## Instalación

Para la instalación del mismo existen varias formas, las cuales se ven a continuación.


### Desde un repositorio de charts


Primero agregar el repositorio a los repositorios locales:

`helm repo add pruebaRepo https://github.com/giachino/kubernetesFingProject/raw/create_repo/fingHelmPackage`

Luego de agregar el repo con nombre "pruebaRepo" podemos instalar el chart en el paquete "fingHelmChart"
y hacer que localmente ese deploy tenga nombre "miDeploy":

`helm install miDeploy pruebaRepo/fingHelmChart`

### Desde un archivo de chart local

Teniendo el package de forma local 

`helm install miDeploy fingHelmChart-1.0.0.tgz`

### Desde un directorio de chart descomprimido

Si hacemos refencia al directorio raíz local del chart, podemos instalarlo así:

`helm install miDeploy path/to/fingHelmChart`

### Desde una URL completa

Con la URL absoluta al archivo de package:

`helm install miDeploy https://github.com/giachino/kubernetesFingProject/raw/create_repo/fingHelmPackage/fingHelmChart-1.0.0.tgz`


## Desintalación

Para desinstalar el chart que instalamos de nombre "miDeploy":

`helm repo remove pruebaRepo`