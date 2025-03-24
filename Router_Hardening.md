
# Introducción

El **hardening** de un router implica aplicar una serie de configuraciones y medidas de seguridad para protegerlo contra posibles ataques y garantizar la integridad de la red. En el caso del **Asus ZenWiFi AX**, el router que hemos escogido en esta práctica, es importante reforzar su seguridad para aprovechar al máximo sus prestaciones sin comprometer la protección.
# Router Hardening

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image.png]]

Primero, nos dirigimos a la pestaña "AiProtection", que nos permite monitorizar la red en tiempo real para detectar malware, virus e intrusiones antes de que alcancen nuestra red.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-1.png]]

Hacemos clic en "Network Protection".

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-2.png]]

Habilitamos la AiProtectition.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-3.png]]

Le damos a "Scan" para iniciar una evaluación de la seguridad de nuestro router.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-4.png]]

Nos avisa de que aún tenemos los credenciales por defecto, también que la contraseña Wi-Fi no es lo suficientemente segura, el WPS sigue habilitado y es inseguro y no está activado el bloqueo de sitios web maliciosos en la red.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-5.png]]

Le hacemos clic a "No" y nos dirigimos al lugar donde modificar la contraseña del administrador y establecemos una segura.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-6.png]]

Bajamos y le damos a "Apply" para guardar los cambios. La contraseña se usará en el próximo inicio de sesión en el router.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-7.png]]

Deshabilitamos WPS para evitar ataques de fuerza bruta de posibles atacantes.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-8.png]]

También desactivamos UPnP cuando no lo usemos para que no puedan acceder a través del puerto abierto.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-9.png]]

Ahora vamos a modificar el método de autenticación a uno más seguro. Nos dirigimos a "Network Map" y seleccionamos "WPA2/WPA3-Personal".

También hacemos lo mismo para 5 GHz en el caso en que la tuvieramos activada.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-10.png]]

Nos dirigimos a la pestaña de "Administration" y luego a la opción de "System".

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-11.png]]

El parámetro de "Enable Login Captcha" que hace que sólo las personas puedan acceder lo mantenemos activo.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-12.png]]

Modificamos el tiempo en que se cierra sesión a 10 minutos.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-13.png]]

Aplicamos los cambios.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-14.png]]

Ahora vamos a "Guest Network".

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-15.png]]

Hacemos clic en "Enable".

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-16.png]]

Tenemos el siguiente panel de invitado en que configuramos su contraseña propia de WAP2/WPA3-Personal.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-17.png]]

Ahora configuramos el Firewall en la siguiente opción.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-18.png]]

Activamos la protección DoS y aplicamos los cambios.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-19.png]]

Volviendo al apartado "Administration", configuramos las actualizaciones del Firmware del router.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-20.png]]

> Nota: En una versión real de la configuración de este router, podemos activar la actualización automática del Firmware asignándole un horario incluso.

Volvemos a "System" y activamos la opción de acceder mediante HTTPS también a la página de configuración. Aplicamos los cambios como siempre.

![[Bastionado_de_Sistemas/UD4/Proyecto_8_Seguridad_en_conexiones_invisibles/images/image-21.png]]

# Comparación con una guía oficial

A partir del modelo **Asus ZenWiFi AX**, buscamos una [guía oficial de hardening](https://www.asus.com/support/faq/1039292/). Se destacan los siguientes puntos clave:

- Activar la encriptación WPA2-AES.
- Establecer contraseñas separadas para la red wifi y la Web GUI.
- Usar contraseñas largas y complejas.
- Actualizar el firmware a la última versión.
- Activar el firewall.
- Activar AiProtection.
- Desactivar el acceso desde WAN para que no se pueda acceder al router desde Internet.
- Desactivar Telnet y SSH.
- No activar la DMZ.
- Habilitar la protección de DNS Rebind.
- Habilitar el acceso por HTTPS a la Web GUI.
- Sólo permitir el acceso con IP's especificadas.
- Desactivar UPnP.
- Configuración del Filtro de Direcciones MAC Inalámbricas para la red inalámbrica.

En mi guía del apartado anterior de hardening he establecido que la encriptación sea WP2/WP3-Personal, ya que permite una configuración más directa y menos dependiente de infraestructuras adicionales, lo que facilita la gestión de la red. El uso de WPA3 en entornos compatibles, permite mejoras significativas en la protección contra ataques de fuerza bruta.

Además, lo de no activar la DMZ, es cierto que evita exponer dispositivos sin protección a la red, pero en ocasiones la DMZ es utilizada para alojar servicios que necesitan acceso público, sobre todo en una empresa. Se debería configurar, en vez de deshabilitarla.

# Conclusión

Este proyecto me ha permitido profundizar un poco en la configuración y el hardening de un router Asus, de los cuales no tenía conocimiento alguno, integrando medidas de seguridad y evaluando alternativas tras leer la guía oficial de hardening.