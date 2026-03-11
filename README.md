# Nessus Expert
En esta sección detallo los motivos por los cuales he seleccionado Nessus Expert para este laboratorio, destacando sus capacidades de visibilidad sobre la superficie de ataque moderna

## Introducción

En este proyecto, realizo una auditoría de seguridad utilizando Nessus Expert sobre un entorno controlado en Windows 11. Mi objetivo es demostrar la capacidad de identificar, clasificar y priorizar vulnerabilidades tanto en activos internos como en la superficie de ataque externa. Esta práctica simula un flujo de trabajo real de un analista de ciberseguridad, desde la fase de reconocimiento hasta la propuesta de remediación.

## ¿Por qué utilizar Nessus Expert?

He seleccionado la versión Expert frente a la Professional o Essentials por su capacidad de ir más allá de la red tradicional. Como estoy documentando una auditoría integral, necesito las funciones exclusivas que esta versión ofrece:

### Comparativa Técnica: Nessus Expert

| Característica | Ventajas (Pros) | Desventajas (Contras) |
| :--- | :--- | :--- |
| **Visibilidad Externa** | **EASM:** permite descubrir activos en internet que no están inventariados. | Requiere configuración DNS precisa; si no, los resultados son limitados. |
| **Infraestructura Cloud** | **Escaneo de IaC:** audita plantillas de Terraform o CloudFormation antes del despliegue. | La versión de prueba limita la profundidad de análisis en la nube. |
| **Priorización de Riesgos** | **Métrica VPR:** prioriza vulnerabilidades según la probabilidad real de explotación. | Requiere conexión constante a Tenable para actualizar inteligencia de amenazas. |
| **Escalabilidad** | Permite gestionar hasta 32 hosts en la versión Trial, ideal para auditorías específicas. | El límite de 32 hosts es insuficiente para redes corporativas medianas. |
| **Facilidad de Uso** | Interfaz intuitiva sobre Windows 11 con reportes ejecutivos profesionales. | El consumo de RAM de `nessusd.exe` es elevado durante escaneos intensivos. |

## Guía de Instalación y Configuración

Para replicar este entorno de auditoría en **Windows 11**, sigo estos pasos de manera secuencial:

1. **Descarga de software:** obtengo el instalador oficial de **Nessus Expert** directamente desde el portal de descargas de Tenable, seleccionando la arquitectura compatible con mi sistema.
2. **Ejecución del instalador:** ejecuto el archivo `.msi` y sigo las instrucciones del asistente de instalación. Durante este proceso, verifico que el servicio `nessusd` se inicie correctamente en el sistema.
3. **Activación de la instancia:** accedo a la interfaz web a través de la dirección `https://localhost:8834`. Utilizo mi clave de licencia **Trial** (limitada a 32 hosts) para completar el registro y activar todas las capacidades de la versión Expert.
4. **Actualización crítica de Plugins:** una vez activado, espero a que la herramienta descargue e instale las últimas definiciones de vulnerabilidades. Considero este paso fundamental para garantizar que los resultados del escaneo sean precisos y detecten las amenazas más recientes.


## Ejemplo de uso: auditoría de red local

Como ejemplo práctico de uso, configuro un escaneo de red básico.
- Metodología: selecciono la plantilla básica para maximizar la compatibilidad y el descubrimiento de servicios.
- Objetivos: configuro mis activos locales (router y host principal), manteniéndome dentro del límite de 32 hosts de mi licencia.
- Ejecución: inicio el escaneo y monitorizo en tiempo real la pestaña de Vulnerabilities para observar la criticidad de los servicios detectados.
