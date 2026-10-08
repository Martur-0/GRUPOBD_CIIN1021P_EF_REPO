# GRUPOBD_CIIN1021P_EF_REPO

+-NUESTRA REFLEXIÓN-+

Asumir el desarrollo del proyecto DataSalud Perú para la DIRESA La Libertad nos ha hecho comprender que, detrás de los más de 40 millones de registros históricos del MINSA, no hay simples filas de datos, sino historias clínicas, identidades y vulnerabilidades de pacientes reales. Guiados por el Código de Ética del Colegio de Ingenieros del Perú, reconocemos que nuestra responsabilidad trasciende la simple implementación técnica; se trata de garantizar que la tecnología esté al servicio del bienestar social y respete la dignidad humana. En este sentido, la arquitectura de nuestra base de datos no es neutral, ya que cada decisión de diseño tiene un impacto directo sobre las personas.
Durante el proceso, nos enfrentamos a dilemas éticos que requirieron decisiones fundamentadas:

°PRIMER DILEMA-PRIVACIDAD DEL PACIENTE FRENTE A LA A NALITICA:
  
El primer gran reto fue decidir qué tan accesibles debían ser los datos para el equipo de la DIRESA. Al inicio, parecía más ágil dejar permisos amplios para facilitar la creación rápida de dashboards. Sin embargo, esto exponía a los pacientes a posibles filtraciones o consultas no autorizadas sobre su estado de salud, infringiendo la Ley N.° 29733 de Protección de Datos Personales.
Nuestras deciciones fueron priorizar la privacidad mediante un diseño estricto de segregación de roles (administrador, analista de datos, auditor) y la implementación de triggers de auditoría.
La concreta conscecuencia de esta decisión es que protegemos a los pacientes contra el uso indebido de su información médica, evitando que sufran discriminación o exposición, aunque esto signifique que el equipo de salud deba seguir protocolos más estrictos para acceder a la base de datos.


°NUESTRO SEGUNDO DILEMA-LA CALIDAD DE LOS DATOS Y LA DISTRIBUCION DE LOS RECURSOS:

Al analizar los reportes de los 312 establecimientos de salud, notamos una cantidad masiva de valores nulos y registros duplicados. El dilema ético aquí era si debíamos omitir estos registros Sucios para que el dashboard de Power BI se viera más limpio y funcional rápidamente, o si debíamos procesarlos. Lo que hicimos fue implementar procesos ETL rigurosos y procedimientos almacenados con control de excepciones para limpiar y validar la ingesta, en lugar de simplemente eliminar los datos conflictivos. La **consecuencia concreta** de esta decisión impacta vitalmente a la comunidad: si hubiéramos eliminado los registros incompletos, los KPIs del dashboard podrían haber subrepresentado la necesidad real de ciertas provincias. Un indicador sesgado podría llevar al director regional a enviar menos vacunas o personal a una zona vulnerable, afectando directamente el derecho a la salud de esa población.



°TRAYECTORIA DE APRENDIZAJE DE NUESTROS FUNDAMENTOS A NUESTRO FUTURO PROFESIONAL:

Para poder construir soluciones éticas y técnicamente viables, este proyecto integrador se ha apoyado fuertemente en nuestra trayectoria académica. De manera explícita, declaramos que hemos retomado saberes previos del curso Base de Datos (ciclo 3). Específicamente, aplicamos los fundamentos de modelado relacional (entidad-relación), la normalización de tablas para evitar redundancias, y la creación de consultas SQL básicas, los cuales sirvieron como cimientos para entender cómo estructurar el Data Warehouse bajo la metodología de Kimball y cómo diseñar nuestras tablas de hechos y dimensiones.   Asimismo, el nivel de exigencia de este desafío nos deja preparados para cursos posteriores (Ciencia de Datos, Ingeniería de Software). Para Ciencia de Datos, el uso de Apache Spark y el procesamiento de datos masivos semiestructurados nos ha dado la base necesaria para, en el futuro, entrenar modelos predictivos sobre grandes volúmenes de información médica. Por otro lado, para Ingeniería de Software, el haber trabajado con control de versiones en GitHub, manejado transacciones complejas (COMMIT/ROLLBACK) y evaluado la latencia y escalabilidad entre entornos SQL y NoSQL, nos prepara para diseñar arquitecturas de sistemas robustos, resilientes y orientados a resolver problemas reales bajo normativas estrictas
