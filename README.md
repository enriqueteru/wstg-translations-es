# Traduce la versión 4.2 de la Guía de Pruebas de Seguridad de OWASP al español de España.
El texto original en inglés puede encontrarse en: https://github.com/OWASP/wstg/releases/tag/v4.2.

# Cómo contribuir a esta traducción

Al enviar un *Pull Request* [pull request](#how-to-submit-a-pull-request), revisores y editores deben asociar los cambios a una sección:

1. Elige una sección que te gustaría revisar.
2. Clona el repositorio y envía un *Pull Request* desde una rama llamada `revisa-<número>`.  
   Por ejemplo:  
   `git checkout -b revisa-4-01-07`

# Índice

## 0. [Prólogo por Eoin Keary](0-Prologo/README.md)

## 1. [Frontispicio](1-Frontispicio/)

## 2. [Introducción](2-Introduccion/)

### 2.1 [El Proyecto de Pruebas de OWASP](2-Introduccion/README.md#el-proyecto-de-pruebas-de-owasp)

### 2.2 [Principios de prueba](2-Introduccion/README.md#principios-de-prueba)

### 2.3 [Técnicas de prueba explicadas](2-Introduccion/README.md#tecnicas-de-prueba-explicadas)

### 2.4 [Inspección manual y revisiones](2-Introduccion/README.md#inspeccion-manual-y-revisiones)

### 2.5 [Modelado de amenazas](2-Introduccion/README.md#modelado-de-amenazas)

### 2.6 [Revisión de código fuente](2-Introduccion/README.md#revision-de-codigo-fuente)

### 2.7 [Pruebas de penetración](2-Introduccion/README.md#pruebas-de-penetracion)

### 2.8 [La necesidad de un enfoque equilibrado](2-Introduccion/README.md#la-necesidad-de-un-enfoque-equilibrado)

### 2.9 [Obtención de requisitos de pruebas de seguridad](2-Introduccion/README.md#obtencion-de-requisitos-de-pruebas-de-seguridad)

### 2.10 [Integración de pruebas de seguridad en el ciclo de desarrollo y pruebas](2-Introduccion/README.md#integracion-de-pruebas-de-seguridad-en-el-ciclo-de-desarrollo-y-pruebas)

### 2.11 [Análisis de datos y generación de informes de seguridad](2-Introduccion/README.md#analisis-de-datos-y-generacion-de-informes-de-seguridad)

## 3. [Marco de pruebas OWASP](3-Marco-Pruebas-OWASP/)

### 3.1 [Marco de pruebas de seguridad en aplicaciones web](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md)

### 3.2 [Fase 1: Antes del desarrollo](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md#fase-1-antes-del-desarrollo)

### 3.3 [Fase 2: Durante la definición y diseño](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md#fase-2-durante-la-definicion-y-diseno)

### 3.4 [Fase 3: Durante el desarrollo](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md#fase-3-durante-el-desarrollo)

### 3.5 [Fase 4: Durante el despliegue](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md#fase-4-durante-el-despliegue)

### 3.6 [Fase 5: Mantenimiento y operaciones](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md#fase-5-mantenimiento-y-operaciones)

### 3.7 [Flujo de trabajo típico de pruebas en SDLC](3-Marco-Pruebas-OWASP/0-Marco-Pruebas-Seguridad-Web.md#flujo-de-trabajo-tipico-de-pruebas-en-sdlc)

### 3.8 [Metodologías de pruebas de penetración](3-Marco-Pruebas-OWASP/1-Metodologias-Pruebas-Penetracion.md)

## 4. [Pruebas de seguridad en aplicaciones web](4-Pruebas-Seguridad-WebApps/)

### 4.0 [Introducción y objetivos](4-Pruebas-Seguridad-WebApps/00-Introduccion-y-Objetivos/README.md)

### 4.1 [Recopilación de información](4-Pruebas-Seguridad-WebApps/01-Recopilacion-Informacion/README.md)

### 4.2 [Pruebas de configuración y gestión de despliegue](4-Pruebas-Seguridad-WebApps/02-Pruebas-Configuracion-Despliegue/README.md)

### 4.3 [Pruebas de gestión de identidades](4-Pruebas-Seguridad-WebApps/03-Pruebas-Gestion-Identidades/README.md)

### 4.4 [Pruebas de autenticación](4-Pruebas-Seguridad-WebApps/04-Pruebas-Autenticacion/README.md)

### 4.5 [Pruebas de autorización](4-Pruebas-Seguridad-WebApps/05-Pruebas-Autorizacion/README.md)

### 4.6 [Pruebas de gestión de sesiones](4-Pruebas-Seguridad-WebApps/06-Pruebas-Gestion-Sesiones/README.md)

### 4.7 [Pruebas de validación de entradas](4-Pruebas-Seguridad-WebApps/07-Pruebas-Validacion-Entradas/README.md)

### 4.8 [Pruebas de manejo de errores](4-Pruebas-Seguridad-WebApps/08-Pruebas-Manejo-Errores/README.md)

### 4.9 [Pruebas de criptografía débil](4-Pruebas-Seguridad-WebApps/09-Pruebas-Criptografia-Debil/README.md)

### 4.10 [Pruebas de lógica de negocio](4-Pruebas-Seguridad-WebApps/10-Pruebas-Logica-Negocio/README.md)

### 4.11 [Pruebas del lado del cliente](4-Pruebas-Seguridad-WebApps/11-Pruebas-Lado-Cliente/README.md)

### 4.12 [Pruebas de API](4-Pruebas-Seguridad-WebApps/12-Pruebas-API/README.md)

## 5. [Informes](5-Informes/README.md)

## 6. [Apéndice](6-Apendice/README.md)

### Apéndice A. [Herramientas de prueba](6-Apendice/A-Herramientas-Prueba.md)

### Apéndice B. [Lecturas recomendadas](6-Apendice/B-Lecturas-Recomendadas.md)

### Apéndice C. [Fuzzing](6-Apendice/C-Fuzzing.md)

### Apéndice D. [Inyecciones codificadas](6-Apendice/D-Inyecciones-Codificadas.md)

### Apéndice E. [Historial del proyecto](6-Apendice/E-Historial.md)

### Apéndice F. [Uso de herramientas de desarrollo en el navegador](6-Apendice/F-Herramientas-Desarrollo-Navegador.md)
