# SCADA 4.0 · Hitech INGENIUM 


Sistema SCADA desarrollado en Flutter. Diseñado para el monitoreo, control en tiempo real, telemetría y auditoría de celdas de manufactura automatizadas, estaciones neumáticas, robots de 3 ejes, centros de maquinado y prensas industriales.

##  Características Principales


* **Estación Neumática:** Control y monitoreo de actuadores, presiones y válvulas.
* **Robot de 3 Ejes:** Visualización de coordenadas, ciclos de operación y estados de efectores.
* **Centro de Maquinado:** Monitoreo de velocidad de husillo, temperatura y avance de corte.
* **Estación de Prensado:** Control de fuerza aplicada, límites de carrera y ciclos de prensado.
* **Telemetría y Analíticas en Tiempo Real:** Gráficos interactivos de rendimiento, conteo de piezas procesadas, tiempos de ciclo y métricas OEE utilizando `fl_chart` y `syncfusion_flutter_gauges`.
* **Comunicación Industrial (IoT):** Integración con protocolos en tiempo real mediante `mqtt_client` y `web_socket_channel` para la conexión directa con PLCs y pasarelas IoT.
* **Sincronización Cloud y Offline:** Integración robusta con **Cloud Firestore** con soporte de persistencia offline (`persistenceEnabled: true`), garantizando continuidad operativa ante pérdida de red.
* **Seguridad y Control de Accesos (RBAC):** Autenticación de operadores y administradores con cifrado seguro de credenciales mediante `bcrypt` y persistencia de sesión con `SharedPreferences`.
* **Auditoría y Historial de Alertas:** Registro detallado de eventos críticos, paros de emergencia, resets de sistema y bitácoras con marcas de tiempo (`timestamps`).
* **Generación de Reportes:** Herramienta integrada para exportación de reportes operativos en formato PDF.


## Stack Tecnológico

* **Framework & UI:** Flutter (Material Design 3, Dark Industrial Theme), `Provider` (Gestión de estado).
* **Navegación:** `go_router` / Navegación estructurada.
* **Backend & Base de Datos:** Firebase Core, Cloud Firestore, Firebase Storage.
* **Protocolos & Conectividad:** MQTT (`mqtt_client`), WebSockets (`web_socket_channel`), HTTP.
* **Visualización de Datos:** `fl_chart`, `syncfusion_flutter_gauges`, `flutter_animate`.
* **Seguridad & Utilidades:** `bcrypt`, `shared_preferences`, `intl`, `pdf`, `printing`, `connectivity_plus`.



## Estructura del Proyecto

```text
lib/
├── main.dart                 # Punto de entrada, inicialización de Firebase y AuthGuard
├── auth_guard.dart           # Control de sesión y redirección protegida
├── login.dart                # Pantalla de autenticación y gestión de usuarios
├── home.dart                 # Dashboard principal y enrutador de vistas HMI
├── firebase_service.dart     # Capa de datos para Firestore, telemetría y auditoría
├── analitycs.dart            # Módulo de métricas y gráficos analíticos
├── conexiones_grid.dart      # Monitoreo en rejilla de conexiones de hardware
├── conexiones_tablas.dart    # Tablas de estado de red y pasarelas
├── diagnostico_conexiones.dart # Herramientas de diagnóstico de red y PLCs
├── scada_neumatico.dart      # HMI Estación Neumática
├── main_robot_3_ejes.dart    # HMI Robot Cartesiano / 3 Ejes
├── main_maquinados.dart      # HMI Centro de Maquinado CNC
├── main_prensado.dart        # HMI Estación de Prensado Hidráulico
├── historialylogs.dart       # Bitácora de eventos y paros de emergencia
├── usuarios.dart             # Administración de usuarios y permisos
├── nuevousuario.dart         # Registro de nuevos operadores/técnicos
└── nube.dart                 # Estado de sincronización cloud
```
