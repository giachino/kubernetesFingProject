# kubernetesFingProject

Proyecto de fin de curso kubernetes - Facultad de Ingeniería - UdelarR

Este proyecto genera un chart helm, el cual hace un despliege automático 
de una aplicación en tres capas en kubernetes.


## Instalación

Para la instalación del mismo existen varias formas, las cuales se ven a continuación.


### Desde un repositorio de charts


    * Primero agregar el repositorio a los repositorios locales:

    `helm repo add pruebaRepo https://github.com/giachino/kubernetesFingProject/raw/create_repo/fingHelmPackage`

    Luego de agregar el repo con nombre "pruebaRepo" podemos instalar el chart en el paquete "fingHelmChart"
    y hacer que localmente ese deploy tenga nombre "miDeploy":

    `helm install miDeploy pruebaRepo/fingHelmChart`

    *Un archivo de chart local (helm install foo foo-0.1.1.tgz)
    *Un directorio de chart descomprimido (helm install foo path/to/foo)
    *Una URL completa (helm install foo https://example.com/charts/foo-1.2.3.tgz)


## Desintalación

helm repo remove pruebaRepo