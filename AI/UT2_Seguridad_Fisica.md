---
title: "Seguridad Física en Equipos y Servidores — Tema 2"
institute: "IES Gaspar Melchor de Jovellanos - Fuenlabrada"
professor: "Francisco Javier Hernández Ferreiro"
date: 2026-05-04
license: "CC BY-SA 4.0"
---

# Seguridad Física en Equipos y Servidores — Tema 2

## Portada
Instituto: IES Gaspar Melchor de Jovellanos - Fuenlabrada
Profesor: Francisco Javier Hernández Ferreiro
Curso: Seguridad Informática (SMR)
Fecha: 2026-05-04
Licencia: CC BY-SA 4.0

## Índice
1. Introducción
2. Modelos de red: SoHo y Workgroups
3. Servidores: rol y consideraciones físicas
4. Seguridad física: conceptos y amenazas
  4.1 Control de acceso físico
  4.2 Videovigilancia (CCTV) y privacidad
  4.3 Personal de vigilancia
  4.4 Alarmas e detección (intrusión e incendio)
  4.5 Protección ambiental: fuego, agua, temperatura y humedad
  4.6 Suministro eléctrico y UPS
  4.7 Cableado, racks y puesta a tierra
  4.8 Seguridad de medios y backups
5. Detección y trazabilidad: logs físicos y evidencias
6. Normativa y privacidad (RGPD / LOPDGDD / seguridad privada)
7. Buenas prácticas y checklist
8. Casos reales y ejemplos recientes
9. Guía de laboratorio y actividades prácticas (2 sesiones)
10. Evaluación y rúbrica
11. Glosario
12. Bibliografía y recursos
13. Anexos


## 1. Introducción
En entornos altamente conectados la superficie de ataque aumenta: pérdidas físicas, sabotaje, fallos ambientales y manipulaciones del equipo suponen riesgos reales para la seguridad de la información.
La arquitectura cliente/servidor centraliza servicios y datos en servidores; esto facilita administración pero exige medidas físicas para proteger esos activos.

**Objetivos del tema:**
- Conocer las amenazas físicas que afectan a equipos y servidores.
- Diseñar controles preventivos y detectivos básicos.
- Aplicar buenas prácticas en la gestión de salas de servidores y equipos sensibles.


## 2. Modelos de red: SoHo y Workgroups
**SoHo / Workgroup**: entornos sin servidores dedicados. Cada estación comparte recursos y puede actuar como servidor.

**Ventajas:** bajo coste, facilidad de despliegue.
**Desventajas:** descentralización de datos, difícil control, aumento de riesgos por multiplicación de puntos de fallo.

**Recomendación:** centralizar datos sensibles en un servidor o almacenamiento controlado y con copias de seguridad.


## 3. Servidores: rol y consideraciones físicas
Un servidor es un rol: cualquier equipo puede ser servidor. Sin embargo, los servidores deben ubicarse en salas con condiciones controladas (temperatura, humedad, alimentación, seguridad perimetral).

Buenas prácticas:
- Racks con cerradura y control de acceso.
- Organización y etiquetado de cables (patch panels).
- Inventario y documentación de hardware y puertos.


## 4. Seguridad física: conceptos y amenazas
Protege la confidencialidad, integridad y disponibilidad desde el plano físico: acceso no autorizado, robo, vandalismo, incendios, inundaciones y fallos ambientales.

Categorías de medidas:
- Preventivas: control de accesos, cerraduras, cámaras, políticas.
- Detectivas: sensores, alarmas, registros.
- Correctivas: extinción, recuperación, backups offline.


### 4.1 Control de acceso físico
Componentes:
- Identificación (algo que se posee / se sabe / biométrico).
- Autorización (perfiles, horarios).
- Trazabilidad (registro/log).

Sistemas típicos: cerraduras mecánicas y electrónicas, tarjetas RFID, PIN, biometría.

Riesgos: clonación de tarjetas, tailgating, bypass de cerraduras. Políticas: desactivar tarjetas perdidas, separar funciones, aplicar principio de mínimo privilegio.


### 4.2 Videovigilancia (CCTV) y privacidad
Papel: disuasión, detección y evidencias. Por sí sola es mayormente detectiva; combinada con vigilancia humana puede actuar de forma activa.

Consideraciones legales: RGPD/LOPDGDD — informar mediante carteles, limitar retención, controlar acceso a grabaciones y cifrar copias.

Buenas prácticas: cambiar credenciales por defecto, segmentar red de cámaras (VLAN), actualizar firmware, restringir acceso remoto.


### 4.3 Personal de vigilancia
Funciones: control de accesos, monitorización de alarmas y respuesta inicial.

En España: vigilancia privada debe ser realizada por empresas autorizadas; las funciones y atribuciones están reguladas.


### 4.4 Alarmas e detección (intrusión e incendio)
Componentes: sensores (movimiento, magnéticos, rotura de cristal, humo/temperatura), módulo central, sirenas y comunicadores (PSTN/GSM/IP/la red primaria y backups).

Diseño: módulo central en caja resistente, batería/UPS, comunicaciones redundantes para evitar inhibidores.

Detectores de incendio: ópticos (humo), térmicos, y detección por aspiración (VESDA) en salas críticas.

Sistemas de extinción: agua nebulizada (cuando es compatible), agentes gaseosos (FM-200, Inergen) en salas sin ocupación prolongada.


### 4.5 Protección ambiental: fuego, agua y condiciones ambientales
Control de temperatura y humedad; sensores de fugas; ubicación adecuada de equipos; separación de zonas de riesgo.

Ejemplo: fallo de climatización que provoca overheating y parada en cascada — necesidad de alarmas ambientales y procedimientos de contingencia.


### 4.6 Suministro eléctrico y UPS
UPS para cortes breves y permitir apagado ordenado; generador para cortes largos.

Prácticas: PDUs monitoreadas, mantenimientos de baterías, pruebas periódicas de autonomía, protección contra sobretensiones.


### 4.7 Cableado, racks y puesta a tierra
Racks cerrados con ventilación y gestión de cables; etiquetado; puesta a tierra y conexión equipotencial.


### 4.8 Seguridad de medios y backups
Soportes sensibles (discos, copias) en cajas fuertes y cifrados; política clara de backups offsite y verificación de restauración.


## 5. Detección y trazabilidad: logs físicos y evidencias
Registros de acceso con retención definida por política; informes de incidentes con cadena de custodia; integración de eventos físicos en SIEM cuando sea posible.


## 6. Normativa, privacidad y requisitos legales
RGPD / LOPDGDD: tratamiento de imágenes de videovigilancia y datos personales. Referencias: ISO/IEC 27001 (Control A.11), INCIBE, CCN-CERT.


## 7. Buenas prácticas y checklist (resumen)
- Sala de servidores: acceso restringido, registro, CCTV, detección de incendios, UPS, ventilación.
- Backups cifrados y offsite.
- Actualizar firmware y eliminar cuentas por defecto.
- Simulacros y formación.


## 8. Casos reales y ejemplos recientes
- Cámaras IP expuestas por credenciales por defecto.
- Fallos de climatización y pérdida de servicio.
- Sabotaje físico a puntos de red en infraestructuras pequeñas.


## 9. Guía de laboratorio y actividades prácticas (2 sesiones)
Sesión 1 (50 min): análisis de plano de sala y checklist; actividad grupal: identificar 10 fallos y priorizarlos.
Sesión 2 (50 min): registro de accesos simulado y auditoría básica de cámaras (inventario y recomendaciones).

Actividades y entregables incluidos en el repositorio.


## 10. Evaluación y rúbrica
- Comprensión teórica: 30%
- Aplicación práctica: 40%
- Documentación: 20%
- Trabajo en equipo: 10%


## 11. Glosario
- CCTV: Circuito Cerrado de Televisión
- UPS/SAI: Sistema de Alimentación Ininterrumpida
- VESDA: Very Early Smoke Detection Apparatus
- Tamper: protección contra manipulación
- Tailgating: entrada aprovechando a persona autorizada


## 12. Bibliografía y recursos
- INCIBE — Guías y recursos para centros educativos
- CCN-CERT — Recomendaciones de seguridad física y ambiental
- ISO/IEC 27001 — Control A.11
- Wikipedia (es) — entradas sobre CCTV, control de accesos, UPS


## 13. Anexos
- Plantilla CSV de registro de accesos
- Checklist imprimible
- Diagrama de ejemplo: sala de servidores (sugerido)
