# Integracion-de-DevOps

## Introducción del Proyecto

Mediante este proyecto se analizarán las competencias prácticas en el uso, configuración e integración de sistemas operativos dentro de entornos virtualizados y contenerizados, aplicando conceptos de DevOps y NetOps. A través del desarrollo de una infraestructura tecnológica simulada, se busca reflejar el desempeño de un ingeniero DevOps con capacidades de administración de redes, encargado de implementar, monitorear y documentar la comunicación entre diferentes dependencias de una empresa tecnológica.

Cada dependencia contará con máquinas virtuales y contenedores específicos, interconectados mediante subredes independientes y supervisados desde un servidor central administrado por Debian. Además, se emplearán herramientas de análisis, monitoreo y gestión.

Se busca integrar los principios de la automatización, el despliegue eficiente y la supervisión continua de servicios, comprendiendo la arquitectura de redes modernas y la administración avanzada de sistemas Linux, pilares fundamentales para la ingeniería DevOps actual.

## Creación de la infraestructura principal

Para la gestión de las dependencias solicitadas por la empresa tecnológica A, se conformo una máquina virtual central con Debian, que cumple la función de administrador y monitor general de todas las dependencias. Luego cada dependencia fue desplegada de acuerdo con lo requerido por la empresa

- Recursos Humanos: Máquina virtual con Arch Linux.

- Tecnología: Máquina virtual con Rocky Linux.

- Financiera: Contenedor con Garuda Linux.

- Comercial y Ventas: Contenedor con Fedora Linux.

Para realizar bien la practica se instalo cada maquina virtual, incluyendo la configuración de red, asignación de IP estática, instalación de dependencias y pruebas de conectividad. Se validó que cada dependencia únicamente pudiera comunicarse con sus propios equipos, mientras que el administrador Debian podía acceder a todas las redes mediante un puente configurado en QEMU.

## Expansión de la arquitectura

Se gestiono la expansión de cada dependencia incorporando nuevas máquinas virtuales y contenedores adicionales:

Recursos Humanos: VM con Manjaro y contenedor con CentOS.

Tecnología: VM con Kali Linux y Linux Mint.

Financiera: Contenedores con Ubuntu y Alpine.

Comercial y Ventas: VM con Alma Linux y contenedor con Debian.

Estas nuevas instancias fueron integradas dentro de sus respectivas subredes, garantizando una comunicación exclusiva interna y su aislamiento del resto de dependencias.
Cada instalación fue acompañada de pruebas de ping, rutas de acceso y visualización de interfaces mediante ip a y nmcli.

## Integración y visualización con Grafana

Con todas las dependencias operativas, se procedió a integrar la herramienta Grafana en el servidor administrador.
Desde allí se configuraron dashboards personalizados que muestran en tiempo real el rendimiento de CPU, memoria, tráfico de red y servicios activos de cada máquina virtual y contenedor.
