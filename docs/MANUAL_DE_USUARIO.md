# 📖 MANUAL DE USUARIO - PLATAFORMA VEXTOR
**Sistema SaaS de Gestión de Flotas Vehiculares, Monitoreo GPS y Optimización Logística**

---

## 📌 TABLA DE CONTENIDOS
1. [Introducción y Propósito del Sistema](#1-introducción-y-propósito-del-sistema)
2. [Roles de Usuario y Permisos](#2-roles-de-usuario-y-permisos)
3. [Acceso al Sistema y Seguridad de la Cuenta](#3-acceso-al-sistema-y-seguridad-de-la-cuenta)
   - 3.1. Inicio de Sesión (Login)
   - 3.2. Registro de Nuevos Usuarios
   - 3.3. Recuperación de Contraseña
   - 3.4. Cambio Obligatorio de Contraseña
   - 3.5. Gestión de Sesiones Activas
4. [Módulo de Dashboard / Panel Principal](#4-módulo-de-dashboard--panel-principal)
5. [Módulo de Gestión de Vehículos](#5-módulo-de-gestión-de-vehículos)
   - 5.1. Listado y Filtros del Parque Automotor
   - 5.2. Registrar un Nuevo Vehículo
   - 5.3. Edición y Eliminación de Vehículos
   - 5.4. Estados Operativos del Vehículo
6. [Módulo de Gestión de Conductores](#6-módulo-de-gestión-de-conductores)
   - 6.1. Registro y Consulta de Conductores
   - 6.2. Licencias de Conducción Colombianas
   - 6.3. Estados del Conductor
7. [Módulo de Rutas y Monitoreo GPS en Tiempo Real](#7-módulo-de-rutas-y-monitoreo-gps-en-tiempo-real)
   - 7.1. Programación y Asignación de Rutas con Enrutamiento OSRM
   - 7.2. Monitoreo en Mapa Interactivo (Capa de Tráfico TomTom)
   - 7.3. Seguimiento en Tiempo Real vía WebSockets
8. [Módulo de Gestión de Mantenimiento](#8-módulo-de-gestión-de-mantenimiento)
   - 8.1. Registro de Órdenes de Trabajo (Preventivo / Correctivo)
   - 8.2. Control de Costos en Pesos Colombianos (COP)
   - 8.3. Actualización de Estados de Mantenimiento
9. [Módulo de Reportes Analíticos y Exportación](#9-módulo-de-reportes-analíticos-y-exportación)
   - 9.1. Generación de Reportes
   - 9.2. Exportación a PDF, Excel (XLSX) y CSV
10. [Módulo de Configuración y Administración del Sistema](#10-módulo-de-configuración-y-administración-del-sistema)
    - 10.1. Perfil de Usuario
    - 10.2. Datos Corporativos de la Empresa
    - 10.3. Administración de Usuarios y Roles
    - 10.4. Bitácora de Auditoría (Logs de Actividad)
11. [Flujo Operativo Especializado para Conductores](#11-flujo-operativo-especializado-para-conductores)
    - 11.1. Vista "Mis Rutas"
    - 11.2. Pantalla HUD de Navegación y Transmisión de GPS
12. [Preguntas Frecuentes y Solución de Problemas (FAQ)](#12-preguntas-frecuentes-y-solución-de-problemas-faq)

---

## 1. Introducción y Propósito del Sistema

**VEXTOR** es una solución integral en la nube (SaaS) diseñada para optimizar la logística, el control operativo y la seguridad en la gestión de flotas vehiculares.

Con VEXTOR, su organización puede:
- Rastrear vehículos y conductores en tiempo real sobre mapas interactivos mediante tecnología GPS y WebSockets.
- Calcular rutas óptimas en la malla vial colombiana mediante el motor de enrutamiento OSRM.
- Programar mantenimientos preventivos y correctivos registrando costos detallados en Pesos Colombianos (`COP`).
- Administrar el ciclo de vida del parque automotor y las licencias de conducción de su personal.
- Auditar cada acción dentro de la plataforma y exportar informes ejecutivos en formatos PDF, Excel y CSV.

---

## 2. Roles de Usuario y Permisos

El acceso y las funcionalidades dentro de la plataforma están segmentados según el rol asignado a su cuenta:

| Rol | Descripción y Permisos |
| :--- | :--- |
| **Administrador** | **Acceso Total.** Puede gestionar la flota completa de vehículos, conductores, rutas, mantenimientos, reportes analíticos, auditoría de actividades, datos de la empresa y administración de usuarios y asignación de roles. |
| **Conductor** | **Acceso Operativo.** Diseñado para el personal en campo. Permite visualizar únicamente las rutas asignadas al conductor, iniciar la navegación en tiempo real (HUD) y transmitir la ubicación GPS de forma automática. |
| **Usuario** | **Acceso Básico.** Rol asignado por defecto a los nuevos registros públicos. Permite gestionar únicamente su perfil personal y cambiar su contraseña. Para obtener accesos administrativos u operativos, un Administrador debe cambiar su rol. |

---

## 3. Acceso al Sistema y Seguridad de la Cuenta

### 3.1. Inicio de Sesión (Login)
1. Ingrese a la URL de la plataforma (ej. `http://localhost`).
2. En la pantalla de bienvenida, ingrese su **Correo Electrónico** y **Contraseña**.
3. Haga clic en el botón **"Iniciar Sesión"**.
4. Si las credenciales son correctas, el sistema establecerá una sesión segura e inscripta y lo redirigirá automáticamente a su panel principal.

### 3.2. Registro de Nuevos Usuarios
1. En la pantalla de Login, seleccione el enlace **"¿No tienes cuenta? Regístrate"**.
2. Complete el formulario con su **Nombre Completo**, **Correo Electrónico** y **Contraseña** (mínimo 6 caracteres).
3. Haga clic en **"Crear Cuenta"**.
4. Su cuenta se creará con el rol de **Usuario**. Si requiere permisos de Administrador o Conductor, notifique al Administrador del sistema para la actualización de su perfil.

### 3.3. Recuperación de Contraseña
1. En la pantalla de Login, haga clic en **"¿Olvidaste tu contraseña?"**.
2. Ingrese el correo electrónico registrado en la plataforma.
3. El sistema enviará un enlace de restablecimiento seguro a su correo (válido por 30 minutos).
4. Abra el enlace en su navegador, ingrese su nueva contraseña y confírmela.

### 3.4. Cambio Obligatorio de Contraseña
Si un Administrador ha marcado su cuenta para requerir un cambio de clave obligatorio por políticas de seguridad, al iniciar sesión aparecerá una ventana modal emergente bloqueando la navegación hasta que defina una nueva contraseña segura.

### 3.5. Gestión de Sesiones Activas
En la sección **Ajustes > Seguridad**:
- Podrá visualizar una lista de todas las sesiones abiertas con su cuenta (dispositivo, navegador, dirección IP y última actividad).
- Puede hacer clic en **"Cerrar sesión"** en cualquier dispositivo sospechoso o seleccionar **"Cerrar todas las demás sesiones"**.

---

## 4. Módulo de Dashboard / Panel Principal

El **Dashboard** proporciona una vista panorámica ejecutiva del estado operativo de la empresa en tiempo real:

- **Métricas e Indicadores Clave (KPIs):**
  - Total de vehículos en la flota y desglose por estado (Disponibles, En Ruta, Mantenimiento).
  - Total de conductores activos.
  - Rutas en proceso e historial reciente.
  - Gastos totales acumulados en mantenimiento (`COP`).
- **Mapas y Gráficos Interactivos:** Visualización de tendencias semanales y mensuales de rutas completadas frente a gastos operativos.
- **Acceso Rápido a Notificaciones:** Icono de campana en el encabezado superior para revisar alertas e incidencias recientes.

---

## 5. Módulo de Gestión de Vehículos

Ubicación: Menú lateral ➔ **Vehículos**

### 5.1. Listado y Filtros del Parque Automotor
Muestra la lista de vehículos registrados con información detallada: Placa, Marca, Modelo, Año, Tipo de Vehículo, Capacidad de Carga/Pasajeros, Kilometraje actual y Estado Operativo.
- Dispone de una barra de búsqueda rápida por placa o marca.
- Filtros por estado operativo (`DISPONIBLE`, `EN_RUTA`, `MANTENIMIENTO`, `INACTIVO`).

### 5.2. Registrar un Nuevo Vehículo
1. Haga clic en el botón **"+ Nuevo Vehículo"**.
2. Diligencie los datos requeridos:
   - **Placa:** Identificador único (ej. `ABC-123`).
   - **Marca, Modelo y Año.**
   - **Tipo de Vehículo:** Camión, Furgón, Automóvil, Motocicleta, etc.
   - **Kilometraje Inicial.**
   - **Capacidad de Carga (kg) / Pasajeros.**
3. Haga clic en **"Guardar Vehículo"**.

### 5.3. Edición y Eliminación de Vehículos
- Para editar, haga clic en el icono de lápiz en la fila del vehículo correspondiente.
- Para eliminar, haga clic en el icono de caneca. *Nota: El sistema no permitirá eliminar vehículos que tengan rutas activas o mantenimientos en curso para preservar la integridad de los datos.*

### 5.4. Estados Operativos del Vehículo
- **DISPONIBLE:** El vehículo está apto para asignación de rutas.
- **EN_RUTA:** Asignado a una ruta activa en proceso (se actualiza automáticamente).
- **MANTENIMIENTO:** En taller o revisión técnica (se actualiza automáticamente al crear una orden de trabajo).
- **INACTIVO:** Fuera de servicio.

---

## 6. Módulo de Gestión de Conductores

Ubicación: Menú lateral ➔ **Conductores**

### 6.1. Registro y Consulta de Conductores
Permite administrar la información del personal de conducción: Nombre, Cédula de Ciudadanía/Identificación, Teléfono, Correo Electrónico, Número de Licencia, Categoría y Fecha de Vencimiento de la Licencia.

### 6.2. Licencias de Conducción Colombianas
El sistema valida el formato de las licencias de conducción colombianas (ej. Categorías `A1`, `A2`, `B1`, `B2`, `B3`, `C1`, `C2`, `C3`):
- El sistema alertará visualmente si la licencia de un conductor se encuentra **vencida** o **próxima a vencer**, previniendo riesgos legales en la operación.

### 6.3. Estados del Conductor
- **DISPONIBLE:** Listo para tomar rutas.
- **EN_RUTA:** Ejecutando un trayecto.
- **NO_DISPONIBLE / SUSPENDIDO:** Incapacidad, vacaciones o sanción.

---

## 7. Módulo de Rutas y Monitoreo GPS en Tiempo Real

Ubicación: Menú lateral ➔ **Rutas**

### 7.1. Programación y Asignación de Rutas con Enrutamiento OSRM
1. En la vista de Rutas, haga clic en **"+ Crear Ruta"**.
2. Ingrese el título o descripción de la ruta.
3. Seleccione el **Vehículo** y el **Conductor** a asignar (solo se mostrarán los que estén en estado `DISPONIBLE`).
4. Seleccione en el mapa el **Punto de Origen** y el **Punto de Destino**.
5. El motor **OSRM** trazará automáticamente el trayecto sobre la red vial real de Colombia, calculando la distancia en kilómetros y el tiempo estimado de viaje.
6. Guarde la ruta. Su estado inicial será **`PROGRAMADA`**.

### 7.2. Monitoreo en Mapa Interactivo (Capa de Tráfico TomTom)
- El mapa interactivo permite acercar, alejar y desplazarse por el territorio.
- Cuenta con la opción de activar la **Capa de Tráfico en Tiempo Real (TomTom Traffic)** para evaluar congestiones viales en vivo.

### 7.3. Seguimiento en Tiempo Real vía WebSockets
- En la pestaña **"Conductores en Ruta"**, los administradores pueden observar en tiempo real la ubicación de cada vehículo desplegado en el mapa.
- La posición, velocidad (km/h) y dirección del vehículo se actualizan de forma fluida mediante WebSockets a medida que el conductor transmite su señal GPS desde la aplicación móvil o web.

---

## 8. Módulo de Gestión de Mantenimiento

Ubicación: Menú lateral ➔ **Mantenimiento**

### 8.1. Registro de Órdenes de Trabajo (Preventivo / Correctivo)
1. Haga clic en **"+ Registrar Mantenimiento"**.
2. Seleccione el **Vehículo** a intervenir.
3. Elija el **Tipo de Mantenimiento**:
   - **PREVENTIVO:** Revisiones periódicas, cambio de aceite, alineación, frenos, etc.
   - **CORRECTIVO:** Reparaciones por falla mecánica o colisión.
4. Ingrese la fecha programada, descripción del servicio y el taller de atención.

### 8.2. Control de Costos en Pesos Colombianos (COP)
- Ingrese el costo estimado o final del mantenimiento.
- Todos los valores económicos se manejan y formatean de forma estándar en Pesos Colombianos (`COP`).

### 8.3. Actualización de Estados de Mantenimiento
- **PROGRAMADO:** Mantenimiento agendado a futuro.
- **EN_PROCESO:** El vehículo ingresó al taller (el estado del vehículo cambia a `MANTENIMIENTO`).
- **COMPLETADO:** Trabajo finalizado (el vehículo vuelve a estar `DISPONIBLE` y los costos se suman al histórico).
- **CANCELADO:** Mantenimiento suspendido.

---

## 9. Módulo de Reportes Analíticos y Exportación

Ubicación: Menú lateral ➔ **Reportes**

### 9.1. Generación de Reportes
Permite consultar reportes consolidados según rangos de fecha y categorías:
- **Reporte de Flota y Vehículos:** Kilometraje recorrido, tasa de uso y disponibilidad.
- **Reporte de Rutas Operativas:** Eficiencia de tiempos, rutas completadas vs. canceladas.
- **Reporte Financiero de Mantenimiento:** Costos totales acumulados por vehículo, tipo de servicio y taller.

### 9.2. Exportación a PDF, Excel (XLSX) y CSV
En la parte superior derecha de cada reporte, dispondrá de botones de exportación directa:
- 📄 **Exportar PDF:** Documento formateado con membrete ejecutivo para impresión o presentación.
- 📊 **Exportar Excel (XLSX):** Hoja de cálculo con fórmulas y estilos para análisis avanzado.
- 📝 **Exportar CSV:** Archivo plano delimitado para integración con otros sistemas BI.

---

## 10. Módulo de Configuración y Administración del Sistema

Ubicación: Menú lateral ➔ **Ajustes**

### 10.1. Perfil de Usuario
- Actualice sus datos personales (Nombre, Teléfono).
- Cargue o cambie su foto de perfil.

### 10.2. Datos Corporativos de la Empresa *(Solo Administradores)*
- Configure la Razón Social, NIT, Teléfono, Dirección y Correo de contacto corporativo que aparecerán en los encabezados de los reportes oficiales generados por el sistema.

### 10.3. Administración de Usuarios y Roles *(Solo Administradores)*
- Lista de todos los usuarios registrados en el sistema.
- Permite cambiar el rol de un usuario (ej. promover de `Usuario` a `Administrador` o `Conductor`).
- Permite activar/desactivar cuentas o forzar el cambio de clave en el próximo inicio de sesión.

### 10.4. Bitácora de Auditoría (Logs de Actividad) *(Solo Administradores)*
- Registro inmutable de seguridad que almacena detalladamente cada acción relevante en el sistema: quién la realizó, qué acción ejecutó (Creación, Edición, Eliminación, Login), la dirección IP y la fecha/hora exacta.

---

## 11. Flujo Operativo Especializado para Conductores

Cuando un usuario inicia sesión con el rol de **Conductor**, la interfaz se adapta a un entorno optimizado para operación móvil y conducción:

### 11.1. Vista "Mis Rutas"
- El conductor visualiza una tarjeta clara con las rutas que le han sido asignadas.
- Muestra los detalles clave: Origen, Destino, Hora programada y Distancia estimada.

### 11.2. Pantalla HUD de Navegación y Transmisión de GPS
1. Al presionar **"Iniciar Ruta"**, la aplicación entra en modo **HUD de Navegación**.
2. El sistema solicitará permisos para acceder a la ubicación GPS del dispositivo (`navigator.geolocation`).
3. El mapa centrará automáticamente la posición del vehículo y guiará al conductor por la ruta trazada.
4. De forma transparente, la app transmitirá las coordenadas (Latitud, Longitud, Velocidad en km/h y Rumbo) a la central de monitoreo.
5. Al llegar al destino, el conductor presiona **"Finalizar Ruta"** para cerrar el ciclo operativo y liberar el vehículo.

---

## 12. Preguntas Frecuentes y Solución de Problemas (FAQ)

### ❓ No puedo asignar un vehículo a una nueva ruta, ¿a qué se debe?
> **Respuesta:** Verifique el estado del vehículo. Si el vehículo ya está asignado a otra ruta activa (`EN_RUTA`) o se encuentra en taller (`MANTENIMIENTO`), el sistema bloqueará la asignación para evitar sobreagendamientos.

### ❓ El mapa no calcula la ruta vial entre el origen y el destino.
> **Respuesta:** Asegúrese de que ambos puntos seleccionados estén dentro del territorio cubierto por la red vial o verifique el estado del servicio de enrutamiento OSRM en la central de soporte técnico.

### ❓ ¿Cómo solicito permisos de Administrador para mi cuenta nueva?
> **Respuesta:** Al registrarse por primera vez, el sistema asigna el rol `Usuario`. Solicite a un Administrador activo de su empresa que ingrese a **Ajustes > Gestión de Usuarios** y cambie su rol a **Administrador**.

### ❓ Olvidé mi contraseña de acceso.
> **Respuesta:** En la pantalla de inicio de sesión, haga clic en **"¿Olvidaste tu contraseña?"**, ingrese su correo registrado y siga las instrucciones del enlace enviado a su bandeja de entrada.

---
*VEXTOR Fleet Platform — Manual de Usuario v1.0*
