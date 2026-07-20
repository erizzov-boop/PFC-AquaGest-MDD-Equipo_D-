# PFC-AquaGest-MDD-Equipo_D-
# AquaGest - MDD
## Equipo D

## Descripción del proyecto

**AquaGest** es el sistema de información desarrollado como Proyecto Fin de Curso para la Compañía Biofina (Camaronera El Guasmo). Su propósito es reemplazar el registro manual en papel de las actividades productivas por una plataforma web, con captura de datos vía sensores IoT y un módulo de inteligencia artificial para análisis predictivo (predicción de cosecha óptima, detección de anomalías en el agua, recomendaciones de alimentación).

El sistema completo abarca diez módulos funcionales: Gestión de Estanques, Control de Siembras, Monitoreo del Agua, Alimentación, Historial Sanitario, Gestión de Empleados, Inventario, Mantenimiento, Gestión de Cosechas, Reportes e Inteligencia Artificial — con 25 requisitos funcionales formalizados (RF-01 a RF-25) en la ERS.

---

## Descripción del subsistema modelado: Control de Estanques, Siembras y Seguimiento

**Por qué se eligió este subsistema:** Es la base operativa sobre la que se apoya el resto del ciclo productivo — el monitoreo de agua, la alimentación, la sanidad y la cosecha solo tienen sentido si ya existe un estanque con una siembra activa. Es el módulo con mayor conectividad hacia el resto del sistema.

**Actores involucrados:**

- **Administrador/Coordinador:** Registra estanques, da de alta al personal y valida la capacidad de siembra.
- **Operario de Producción:** Registra cada siembra (fecha, cantidad de larvas, proveedor, responsable) y las sobrecargas controladas.
- **Técnico Acuícola:** Registra los grameos semanales de seguimiento del crecimiento y da seguimiento a las alertas.

**Qué cubre el ciclo de negocio:** Desde el registro de la piscina y el cálculo de su capacidad máxima, pasando por el registro formal de cada siembra y su responsable, hasta el seguimiento semanal del crecimiento del camarón — con sus dos mecanismos de control: el registro de sobrecargas autorizadas cuando la siembra excede la capacidad nominal, y la generación de alertas cuando el crecimiento observado se aparta del esperado.

**Requisitos funcionales cubiertos:** RF-01 a RF-08 (registro de estanque, cálculo de capacidad, sobrecarga controlada, actualización de estado, registro de siembra, grameo semanal, historial de crecimiento, alerta de crecimiento) y RF-17 (registro de empleados, en su rol de responsables de siembra).

**Alcance de la demostración:** Las seis clases de dominio — Estanque, Siembra, Empleado (como responsable), SobrecargaSiembra, Grameo y AlertaCrecimiento — con sus atributos, operaciones y relaciones de asociación, agregación y composición.

**Queda explícitamente fuera de esta demostración puntual:** Monitoreo del Agua, Alimentación, Historial Sanitario (más allá de lo ya cubierto), Inventario, Mantenimiento, Cosecha, Reportes e Inteligencia Artificial — módulos que sí están en el ERS del PFC completo, pero no forman parte del subsistema elegido para esta generación de código.

---

# Herramienta utilizada

- **Herramienta CASE/MDD:** Modelio
- **Versión:** 5.4

---

# Requisitos previos

Para reproducir el proyecto se requiere:

- Modelio 5.4
- Java Development Kit (JDK) 17 o superior
- IntelliJ IDEA Community Edition (o cualquier IDE compatible con Java)
- Sistema Operativo probado:
  - Windows 10
  - Windows 11

---



# Cómo clonar el repositorio

```bash
git clone https://github.com/erizzov-boop/PFC-AquaGest-MDD-Equipo_D-.git
```

Luego ingresar al proyecto:

```bash
cd PFC-AquaGest-MDD-Equipo_D-
```

---

# Cómo abrir el modelo

1. Abrir Modelio 5.4.
2. Seleccionar **Open Project**.
3. Descargar el archivo ubicado en:

```
modelo/AquaGest_ControlSiembras(proyecto exportado desde Modelio).zip
```
---

# Generación automática de código

1. Abrir el proyecto en Modelio.
2. Verificar que el modelo UML se encuentre actualizado.
3. Seleccionar el paquete correspondiente.
4. Ejecutar la opción de generación de código Java desde Modelio.
5. El código generado se almacenará en la carpeta:

```
generado/
```

---

# Compilar el código generado

Abrir el proyecto en IntelliJ IDEA o ejecutar desde consola:

```bash
javac *.java
```

Una vez compilado correctamente, el proyecto estará listo para continuar con la implementación de la lógica de negocio.

---

# Compilar el informe

1. Clonar Repositorio
2. Comprimir carpeta docs en .zip
3. Subir en overleaf



---

# Video demostrativo

El video demostrativo se encuentra en:

```
evidencias/video-demo.mp4
```

Link del video: https://youtu.be/nqC775C5jXs

---

# Integrantes y responsabilidades

| Integrante | Responsabilidad |
|------------|-----------------|
| Rizzo | Modelado UML (Diagrama de clases, generación de código y validación del modelo). |
| Amagua | Diagramas de casos de uso, diagrama de estados y revisión del código generado. |
| Crespo | Documentación en LaTeX, evidencias, repositorio GitHub y preparación de la exposición. |

---

# Créditos

Proyecto desarrollado para la asignatura correspondiente al Proyecto Fin de Curso, aplicando el enfoque **Model-Driven Development (MDD)** mediante la herramienta **Modelio 5.4**.
