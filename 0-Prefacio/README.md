# Prólogo, por Eoin Keary

El problema del software inseguro es quizá el desafío técnico más importante de nuestro tiempo. El crecimiento exponencial de las aplicaciones web, que han impulsado nuevos modelos de negocio, redes sociales, etc., ha hecho más urgente establecer un enfoque sólido para desarrollar y proteger internet, las aplicaciones web y los datos.

En el Open Web Application Security Project® (OWASP®), tratamos de hacer del mundo un lugar donde el software inseguro sea una anomalía, no la norma. La Guía de Pruebas de OWASP tiene un papel fundamental en la resolución de este serio problema. Es de vital importancia que nuestro enfoque para probar la seguridad del software se base en principios de ingeniería y ciencia. Necesitamos una metodología coherente, repetible y claramente definida para realizar pruebas en aplicaciones web. Un mundo sin estándares mínimos en ingeniería y tecnología es un mundo en caos.

No hace falta decir que no se puede crear una aplicación segura sin realizar pruebas de seguridad. Las pruebas forman parte de un enfoque más amplio para construir sistemas seguros. Muchas organizaciones de desarrollo de software no incluyen las pruebas de seguridad en su proceso estándar de desarrollo. Peor aún, muchos proveedores de seguridad ofrecen pruebas con niveles de calidad y rigor muy variables, sin ajustarse a ningún estándar.

Las pruebas de seguridad, por sí solas, no son suficientes para determinar cuán segura es una aplicación, ya que existen infinitas formas en las que puede ser vulnerada. Es simplemente imposible testear todas las combinaciones posibles. No podemos protegernos solo con pruebas cuando tenemos un tiempo limitado para ejecutarlas, mientras que el atacante no tiene esas limitaciones.

Junto con otros proyectos de OWASP, como la Guía de Revisión de Código, la Guía de Desarrollo, y herramientas como [OWASP ZAP](https://www.zaproxy.org), esta guía es un excelente punto de partida para construir y mantener aplicaciones seguras. Te mostrará cómo comprobar la seguridad de una aplicación en ejecución. Recomiendo encarecidamente usar estas guías como parte de cualquier iniciativa de seguridad en aplicaciones.

## ¿Por qué OWASP?

Crear una guía como esta es una tarea titánica, que requiere la experiencia de cientos de personas alrededor del mundo. Existen muchas formas distintas de probar vulnerabilidades, y esta guía recoge el consenso de expertos sobre cómo realizar pruebas de manera eficaz, precisa y rápida. OWASP proporciona a profesionales con ideas afines en el ámbito de la seguridad la posibilidad de colaborar y construir un enfoque común frente a este problema.

La disponibilidad gratuita y abierta de esta guía es clave para la misión de la fundación. Permite que cualquier persona entienda las técnicas utilizadas para identificar fallos de seguridad comunes. La seguridad no debe ser un arte oscuro ni un secreto reservado a unos pocos. Debe estar abierta a todos, incluyendo personal de calidad, desarrolladores y responsables técnicos. Este proyecto pretende mantener ese conocimiento en manos de quienes realmente lo necesitan: tú, yo, y todos los implicados en la creación de software.

Esta guía debe llegar a manos de desarrolladores y testers. No hay suficientes especialistas en seguridad de aplicaciones en el mundo como para abordar el problema a gran escala. La responsabilidad primaria de la seguridad debe recaer sobre los desarrolladores, pues son ellos quienes escriben el código. No debería sorprender que se escriba código inseguro si no se prueban ni consideran las vulnerabilidades que podrían introducirse.

Mantener esta guía actualizada es crucial. Gracias a su formato tipo wiki, la comunidad OWASP puede evolucionar y ampliar el contenido para mantenerse al día ante el rápido cambio del panorama de amenazas.

Esta guía es un testimonio del entusiasmo y la energía de los miembros y voluntarios del proyecto. Sin duda, contribuirá a cambiar el mundo, una línea de código a la vez.

## Adaptar y priorizar

Deberías aplicar esta guía en tu organización. Puedes ajustarla para que se adapte a las tecnologías, procesos y estructura interna de tu equipo.

En general, hay varios perfiles dentro de una organización que pueden utilizar esta guía:

- **Desarrolladores**: para garantizar que escriben código seguro. También pueden desarrollar pruebas como parte de los test unitarios y del flujo de trabajo habitual.
- **Testers y equipos de QA**: para ampliar los casos de prueba existentes. Identificar vulnerabilidades tempranamente ahorra tiempo y esfuerzo posteriormente.
- **Expertos en seguridad**: como complemento a otras técnicas para asegurarse de que no se han pasado por alto fallos críticos.
- **Jefes de proyecto**: para comprender que los problemas de seguridad suelen deberse a defectos de diseño y programación.

La clave al realizar pruebas de seguridad es priorizar. Hay un número infinito de formas en las que una aplicación puede fallar, pero los recursos y el tiempo siempre son limitados. Hay que emplearlos sabiamente, centrándose en vulnerabilidades reales que puedan representar un riesgo concreto para el negocio. Intenta contextualizar los riesgos en función de los casos de uso de la aplicación.

Esta guía debe entenderse como un conjunto de técnicas para encontrar distintos tipos de fallos de seguridad. Pero no todas las técnicas tienen el mismo nivel de importancia. Evita usar la guía como una simple lista de verificación: las amenazas evolucionan constantemente, y ningún listado puede ser definitivo. Sin embargo, es un excelente comienzo.

## El papel de las herramientas automatizadas

Numerosas empresas venden herramientas automáticas para análisis y pruebas de seguridad. Hay que ser conscientes de sus limitaciones y usarlas en lo que realmente son eficaces. Como dijo Michael Howard en la conferencia OWASP AppSec 2006 en Seattle:  
> “¡Las herramientas no hacen que el software sea seguro! Ayudan a escalar el proceso y a aplicar políticas”.

Más aún, estas herramientas son genéricas: no están hechas específicamente para tu aplicación, sino para casos comunes. Esto significa que pueden detectar problemas generales, pero no tienen el conocimiento necesario de tu lógica de negocio y diseño para encontrar fallos más complejos. En mi experiencia, los fallos más críticos están profundamente ligados a la lógica del negocio y al diseño particular del sistema.

Dicho esto, pueden ser muy útiles para detectar errores comunes. Ejecutarlas suele ser rápido, pero analizar y validar cada posible error lleva tiempo. Si tu objetivo es encontrar y corregir las vulnerabilidades más graves lo antes posible, considera si es mejor invertir tiempo en herramientas automáticas o en técnicas manuales como las que describe esta guía. Aun así, estas herramientas son una parte valiosa de un programa de seguridad equilibrado. Usadas correctamente, pueden reforzar tus procesos para producir software más seguro.

## Un llamamiento a la acción

Si construyes, diseñas o pruebas software, te animo encarecidamente a familiarizarte con las prácticas de pruebas de seguridad descritas aquí. Aunque no es una guía definitiva, es un excelente punto de partida para detectar los problemas más comunes que afectan al desarrollo de aplicaciones hoy en día. Si detectas errores, añade una nota en la sección de discusión o edita directamente el contenido. Estarás ayudando a miles de personas que dependen de esta guía.

Por favor, [únete a OWASP](https://owasp.org/membership/) como miembro individual o corporativo para que podamos seguir desarrollando esta guía y muchos otros proyectos.

Gracias a todos los colaboradores anteriores y futuros. Vuestro trabajo contribuirá a hacer del software del mundo un lugar más seguro.

**--Eoin Keary, miembro de la junta directiva de OWASP, 19 de abril de 2013**

Proyecto Libre de Seguridad en Aplicaciones Web y OWASP son marcas registradas de la OWASP Foundation, Inc.
