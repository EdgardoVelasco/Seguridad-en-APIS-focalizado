
# Instalación y configuración

## Instalación
1.	Descarga el software desde aquí, Windows (x86, 32-bit), MSI Installer.
2.	Selecciona no registrarte en esta ocasión, solo descarga, la versión podría cambiar, pero en esencia es 8.0
3.	Inicia el asistente de instalación.

Selecciona la opción de instalación Custom.

![imagen1](../images/image001.png)

Ahora el instalador solicitará qué tipo de instalación se requiere. La elección dependerá del uso que vaya a hacer el software y también de la experiencia que se tenga.
Si va a crear bases de datos desde cero, necesitará utiliza < herramientas de desarrollo y complementos (plugins) para ciertas aplicaciones, por lo que la opción Developer Default o Full pueden ser las adecuadas. En cambio, si únicamente va a cargar bases de datos ya creadas, puede optar por Server Only, para que únicamente se instale el servidor y pueda cargar las bases de datos.
La versión customizada le da la oportudidad de agregar y eliminar elementos que no se requieren, por ejemplo, Visual Studio.

![imagen2](../images/image003.png)

Si elige la opción de Custom podrá seleccionar de forma manual lo que se desea instalar y lo que no de todo el contenido del paquete. Si tiene experiencia o si sabe exactamente lo que vas a necesitar, podrás ahorrar algo de espacio en el ordenador y también evitará instalar cosas que nunca vas a necesitar. Por ejemplo, puedes optar por no instalar la documentación, instalar solo algunos conectores como el de Python o Java, etc.

![imagen3](../images/image005.png)

En este punto es posible que el instalador muestre una lista de software adicional que puede necesitar. Estas dependencias dependerán de las aplicaciones que tenga instaladas en su equipo y también de las partes de MySQL que haya decidido instalar. Solo debes pulsar en Execute y automáticamente se iniciará la descarga e instalación de las dependencias.
Puede pulsar ShowDetails/Hide Details para ver o no ver los detalles de las descargas de dependencias, al finalizar pulse el botón [Next]

![imagen4](../images/image007.png)

Cuando el paso anterior termina, volverá directamente al instalador y noté un listado con los paquetes que se instalaran. Estos son los paquetes elegidos en el paso anteior, sin contar con las dependencias. Verifique que todo es correcto y pulse Execute para iniciar la instalación. 

![imagen5](../images/image009.png) ![imagen1](../images/image011.png)

Ahora el instalador le notifica que debe configurar el servidor. Selección [Next] y automáticamente se insiciará el sistente de configuración.

![imagen6](../images/image013.png)

Ahora tendrá que elegir el tipo de configuración que quiere aplicar al servidor. 
En el menú desplegable Config Type podrás escoger entre las siguientes opciones:
Development Computer: esta configuración está pensada para PCs donde se ejecuta un servidor MySQL con fines de desarrollo, pero que también es utilizado para otras cosas. Consumirá la menor parte posible de los recursos de RAM.
Server Computer: el ordenador no está dedicado exclusivamente a MySQL, pero sí funciona como servidor y no como herramienta de desarrollo. Uso medio de los recursos de memoria.
Dedicated Computer: esta es la opción si el ordenador en el que lo instalas está dedicado exclusivamente a a MySQL. Usará toda la memoria disponible para obtener el mejor rendimiento posible.
Además, puede elegir el puerto a utilizar para acceder al servicio, abrir automáticamente los puertos en el firewall de Windows y cambiar otras opciones más avanzadas. 
En el curso se seleccionará la opción Developtment Computer y deje las valores predeterminados. Una vez elegidas las opciones, selección el botón [Next]

![imagen7](../images/image015.png)

Ahora puede elegir el método de autenticación que se dea usar. El meto que aparece marcado por defecto es más moderno y seguro, por lo que salvo que tenga alguna herramienta que necesite la opción antigüa. Pulse el botoón [Next].

![imagen8](../images/image017.png)

En la nueva ventana que se abre debe establecer la contreseña de acceso a root.
- Contraseña: MySQL_2357

Recuerde usar una contraseña lo más segura posible  (Incluya letras minúsculas, mayúsculas, símbolos y números).

Buena práctica agregar otro usuario admnistrador además de root. En la parte inferior de la pantalla podrá añadir otro usuario; sin embargo puede agregar esas cuentas/usarios más tarde.

Los datos para una cuenta:
- Nombre del usuario: curso
- Host: localhost
- Role: DB Admin
- Contraseña: MySQL_2357

![imagen9](../images/image010.png)
![imagen10](../images/image011.png)

Verá como aparece Configure MySQL Server como Windows Service. Marque esa opción. Podrá escoger el nombre que tendrá el servicio, puede dejar el que trae por defecto o poner uno personalizado.

- Nombre del servicio: MySQL80
- c:\> net [start|stop] MySQL80 

La siguiente opción, Standard System Account recomendado en la mayoría de los casos o elegir un usuario personalizado.

![imagen11](../images/image012.png)

El instalador de MySQL puede asegurar el directorio de datos del servidor actualizando los permisos de archivos y carpetas ubicados en:  C:\ProgramData\MySQL\MySQL Server 8.0\Data

![imagen12](../images/image013.png)

En la ventana podrá ver un resumen de las tareas que va a realizar el configurador. Si está de acuerdo pulse el botón de [Execute] para iniciar la actividad.

![imagen13](../images/image014.png)

Pulse sobre [Finish] para cerrar el configurador y voler al instalador.

![imagen14](../images/image015.png)
![imagen15](../images/image016.png)

El instalador aún podría tener algunas tareas pendientes por instalar y configurar, dependiendo de los paquetes seleccionados y/o modo seleccionado.

![imagen16](../images/image017.png)

Instalación de los esquemas de ejemplo, confirmar la contraseña de root. En el curso se manejó: MySQL_2357

![imagen17](../images/image018.png)
![imagen18](../images/image019.png)
![imagen19](../images/image020.png)

Aún puede haber productos por configurar dependiendo de los paquetes/módulos seleccionados

![imagen20](../images/image021.png)

Puede iniciar MySQL Workbench & MySQL Shell.
	
* MySQL Workbench: Es una herramienta visual de diseño de bases de datos que integra desarrollo de software, administracióin de bases de datos, diseño de bases de datos, gestión y mantenimiento para el sistema de base de datos MySQL.

![imagen21](../images/image022.png)
![imagen22](../images/image023.png)

Herramienta útil que maneja multilenguajes: JavaScript, Python y SQL.

![imagen23](../images/image024.png)


Abra una terminal de comandos (cmd) e ingrese los siguientes comandos para reiniciar el servidro MySQL y aplicar la configuración del proceso, este depende de la versión MySQL 8.0 = mysql80
```
- c:\> net stop mysql80 # Para parar el servidor MySQL
```
```
- c:\> net start mysql80 # Para iniciar el servidor MySQL
```
Para verificar si el servidor MySQL se está ejecutando
```
- c:\> sc query mysql80
```

![imagen24](../images/image025.png)

- [Inicio](../README.md)
