# Levantamiento de Requerimientos Sistema de Gestión de Historias Clínicas

El proceso de levantamiento de requerimientos incluye la identificación de objetivos, usuarios, procesos, integraciones y, de manera fundamental, el levantamiento de casos de uso. Los casos de uso permiten describir cómo interactúan los diferentes actores con el sistema y ayudan a identificar requerimientos funcionales y excepciones.

A continuación las preguntas iniciales para levantar los requerimientos del sistema de gestión de historias clínicas para tratamientos médicos.

## 1. Objetivos del Negocio y Stakeholders
- ¿Cuáles son los objetivos que se desean alcanzar con el sistema de gestión de historias clínicas?
- ¿Quiénes son los stakeholders principales (pacientes, médicos, enfermeros, administradores, especialistas, etc.)?
- ¿Cuáles son los principales problemas o limitaciones del proceso actual de gestión de historias clínicas?

## 2. Usuarios y Roles
- ¿Quiénes son los usuarios del sistema (médicos, enfermeros, especialistas, administradores, pacientes, etc.)?
- ¿Cuáles son los roles de cada usuario?
- ¿Qué permisos necesita cada usuario?
- ¿Los pacientes podrán acceder a sus historias clínicas o solo el personal médico?

## 3. Proceso de Gestión de Historias Clínicas
- ¿Cómo se realiza actualmente la gestión de historias clínicas?
- ¿Qué información es necesaria para crear y mantener una historia clínica (datos del paciente, diagnósticos, tratamientos, medicamentos, etc.)?
- ¿Cuáles son los insumos y documentos necesarios para gestionar una historia clínica?
- ¿Existen restricciones (acceso por especialidad, confidencialidad, permisos, etc.)?
- ¿Cómo se determinan y gestionan los niveles de acceso a la información?
- ¿Se pueden modificar o corregir registros en las historias clínicas? ¿Quién puede hacerlo?
- ¿Qué situaciones generan la actualización de las historias clínicas?

## 4. Notificaciones y Comunicación
- ¿Cómo se notifican a los médicos y pacientes sobre actualizaciones en las historias clínicas?
- ¿Qué canales de comunicación se utilizan (SMS, correo electrónico, notificaciones en app, etc.)?
- ¿Se requieren alertas para medicamentos, citas de seguimiento o resultados de laboratorio?

## 5. Integraciones y Datos
- ¿El sistema debe integrarse con otros sistemas (laboratorio, farmacia, facturación, imágenes médicas, etc.)?
- ¿Qué datos deben importarse o exportarse?
- ¿Existen bases de datos o APIs existentes a las que se deba conectar?

## 6. Reportes y Monitoreo
- ¿Qué reportes o tableros se requieren (historiales de pacientes, estadísticas de tratamientos, seguimiento de medicamentos, etc.)?
- ¿Quién necesita acceso a estos reportes?

## 7. Restricciones y Cumplimiento
- ¿Existen requisitos regulatorios o de cumplimiento (LOPD, GDPR, normativas médicas, etc.)?
- ¿Hay consideraciones de confidencialidad y seguridad de datos médicos?

## 8. Técnicos y Operacionales
- ¿En qué plataformas debe estar disponible el sistema (web, móvil, ambos)?
- ¿Existen requisitos de disponibilidad o rendimiento?
- ¿Cuál es la escala esperada (número de usuarios, pacientes, historias clínicas, etc.)?

## 9. Crecimiento Futuro y Flexibilidad
- ¿Se planea expandir los servicios médicos o especialidades?
- ¿El sistema debe estar preparado para nuevos tipos de tratamientos o flujos de trabajo médico?

## 10. Levantamiento de Casos de Uso

Para cada tipo de usuario, se deben identificar y documentar los principales casos de uso. Se recomienda utilizar el siguiente formato para cada caso de uso:

- **Nombre del caso de uso**
- **Actor(es) involucrado(s)**
- **Descripción breve**
- **Flujo principal**
- **Flujos alternativos o excepciones**
- **Precondiciones**
- **Postcondiciones**

#### Preguntas guía para identificar casos de uso
- ¿Cuáles son las tareas principales que cada tipo de usuario debe poder realizar en el sistema?
- ¿Qué acciones realiza un usuario desde que inicia sesión hasta que termina su interacción?
- ¿Qué excepciones o situaciones especiales pueden ocurrir durante el proceso de gestión de historias clínicas?
- ¿Puede describir paso a paso cómo un médico crea una nueva historia clínica?
- ¿Qué debe hacer un enfermero cuando actualiza los signos vitales de un paciente?
- ¿Qué sucede si un paciente necesita acceder a su información médica?

#### Ejemplos de Casos de Uso

**Caso de Uso 1: Crear nueva historia clínica**
- **Actor(es):** Médico, Sistema
- **Descripción breve:** El médico crea una nueva historia clínica para un paciente que acude por primera vez.
- **Flujo principal:**
  1. El médico accede al sistema y selecciona la opción para crear nueva historia clínica.
  2. Ingresa los datos personales del paciente (nombre, edad, documento de identidad, etc.).
  3. Registra la información médica inicial (motivo de consulta, antecedentes, etc.).
  4. El sistema valida la información y crea la historia clínica.
  5. El sistema asigna un identificador único y notifica la creación exitosa.
- **Flujos alternativos o excepciones:**
  - Si el paciente ya existe en el sistema, se muestra la historia clínica existente.
  - Si los datos ingresados son incorrectos, el sistema solicita corrección.
- **Precondiciones:** El médico debe estar autenticado y tener permisos para crear historias clínicas.
- **Postcondiciones:** Se crea la historia clínica y queda disponible para futuras consultas.

**Caso de Uso 2: Actualizar historia clínica con nuevo tratamiento**
- **Actor(es):** Médico, Sistema
- **Descripción breve:** El médico actualiza la historia clínica de un paciente con un nuevo diagnóstico y tratamiento.
- **Flujo principal:**
  1. El médico busca la historia clínica del paciente.
  2. Selecciona la opción para agregar nueva información médica.
  3. Registra el diagnóstico, tratamiento prescrito y medicamentos.
  4. El sistema valida la información y actualiza la historia clínica.
  5. Se genera un registro de la actualización con fecha y hora.
- **Flujos alternativos o excepciones:**
  - Si hay conflictos con medicamentos existentes, el sistema muestra alertas.
  - Si el paciente tiene alergias, el sistema verifica la compatibilidad.
- **Precondiciones:** El médico debe tener acceso a la historia clínica del paciente.
- **Postcondiciones:** La historia clínica se actualiza y queda registrado el cambio.

**Caso de Uso 3: Consultar historial médico completo**
- **Actor(es):** Médico, Sistema
- **Descripción breve:** El médico consulta el historial médico completo de un paciente para tomar decisiones clínicas.
- **Flujo principal:**
  1. El médico inicia sesión en el sistema.
  2. Busca al paciente por nombre, documento o número de historia clínica.
  3. El sistema muestra el historial médico completo organizado cronológicamente.
  4. El médico puede filtrar por tipo de información (diagnósticos, tratamientos, medicamentos, etc.).
- **Flujos alternativos o excepciones:**
  - Si el paciente no existe, el sistema informa al médico.
  - Si hay información confidencial, el sistema solicita autorización adicional.
- **Precondiciones:** El médico debe estar autenticado y tener permisos para acceder a la información del paciente.
- **Postcondiciones:** El médico visualiza el historial completo y puede tomar decisiones informadas. 