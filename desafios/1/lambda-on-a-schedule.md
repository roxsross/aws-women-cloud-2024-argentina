### Desafío de Laboratorio: Automatización de Gestión de Instancias EC2 con Lambda y CloudWatch

#### Descripción del Desafío:
¡Como futuras arquitectas de soluciones en la nube, es crucial entender cómo diseñar y automatizar arquitecturas que cumplan con los principios del Well-Architected Framework de AWS! En este desafío, tendrás la oportunidad de aplicar estos conocimientos mientras utilizas servicios clave de AWS, como Lambda y CloudWatch, para automatizar la gestión de instancias EC2.

#### Tareas a Realizar:
1. **Diseño de Arquitectura Resiliente:**
   - Diseña una arquitectura que cumpla con los principios de fiabilidad, asegurando que las instancias EC2 estén disponibles y resistentes a fallos.
   - Utiliza grupos de seguridad y configuraciones de red adecuadas para garantizar la seguridad y la conectividad de las instancias EC2.

2. **Configuración de Función Lambda:**
   - En el servicio IAM, crea un rol que siga el principio de seguridad, otorgando permisos mínimos necesarios para la función Lambda.
   - Implementa una función Lambda con el runtime Python version 3.10 en adelante, que siga los principios de eficiencia y excelencia operativa. Asegúrate de utilizar las mejores prácticas de programación y manejo de errores.

3. **Automatización de Gestión de Instancias:**
   - Utiliza la función Lambda para automatizar la gestión de instancias EC2, siguiendo los principios de operaciones sin esfuerzo y automatización.
   - La función Lambda debe verificar el estado de las instancias EC2 y realizar acciones según sea necesario para mantener la integridad y la eficiencia de la arquitectura.

4. **Configuración de Monitoreo y Alertas:**
   - Configura CloudWatch para monitorear el rendimiento y la salud de las instancias EC2, siguiendo el principio de monitoreo continuo.
   - Establece alarmas en CloudWatch para alertar sobre eventos importantes, como la detención o el inicio de instancias EC2.

#### Archivos Adjuntos:
- `lambda_role.json`: [codigo](./lambda_role.json) Política adjunta al rol de ejecución de Lambda, que sigue los principios de permisos mínimos necesarios.
- `lambda_func.py`: [codigo](./lambda_func.py) Función Lambda que implementa la lógica de gestión de instancias EC2, siguiendo los principios de eficiencia y automatización.

#### Notas Adicionales:
- Asegúrate de considerar y aplicar los cinco pilares del Well-Architected Framework de AWS: fiabilidad, seguridad, eficiencia, excelencia operativa y optimización de costos.
- Utiliza la documentación oficial de AWS y las mejores prácticas recomendadas por AWS para guiar tu diseño y configuración.

--- 
Resumen:
1. **Crear una Instancia EC2:**
   - Crea una instancia EC2 de tipo t2.micro y adjunta un grupo de seguridad con reglas de ingreso permitidas para SSH, HTTP y HTTPS.

2. **Configurar un Rol de IAM para Lambda:**
   - En IAM, crea un rol para el servicio Lambda con permisos para realizar amplias acciones en los recursos configurados en la política.

3. **Crear una Función Lambda:**
   - Crea una función Lambda utilizando Python como tiempo de ejecución y asigna el rol de IAM creado anteriormente.
   - Esta función verificará el estado de las instancias EC2 y las modificará según sea necesario (por ejemplo, detenerlas si están en ejecución).

4. **Configurar una Regla en CloudWatch:**
   - En CloudWatch, crea una regla de eventos con una programación fija o un trabajo CRON.
   - Establece la función Lambda como objetivo de la regla de eventos.
   - Edita la configuración de la función Lambda para establecer el tiempo de espera en 1 minuto.
