# MVC_Sistema_Distribuidor

## Sistema Web para la Gestión de Pedidos de Distribuidores

Este repositorio contiene el código fuente de una aplicación web desarrollada bajo el patrón **MVC (Modelo-Vista-Controlador)** con **ASP.NET y C#**, diseñada para optimizar y agilizar el proceso de solicitud de pedidos para clientes de tipo distribuidor.

La aplicación se integra directamente con un sistema ERP existente, leyendo y escribiendo en su base de datos **SQL Server**, lo que garantiza la consistencia de los datos en tiempo real y proporciona a los vendedores una herramienta potente y siempre actualizada.

---

## ✨ Características Principales

Este sistema web ofrece una solución completa para el ciclo de vida de un pedido de distribuidor, incluyendo:

*   **Módulo de Solicitud de Pedidos:** Interfaz centralizada para crear, modificar y gestionar las solicitudes de pedidos.
*   **Gestión de Clientes:** Búsqueda y selección de clientes distribuidores directamente desde la base de datos del ERP.
*   **Control de Crédito y Bloqueo Automático:** El sistema valida en tiempo real el estado de la cartera del cliente. Si un cliente tiene deudas vencidas, se marca como **"CLIENTE BLOQUEADO"** y se restringe la creación de nuevos pedidos, mostrando el detalle de las facturas pendientes.
*   **Catálogo de Artículos:** Búsqueda y selección de productos (artículos) para agregar al pedido, con filtros por modelo y color.
*   **Detalle del Pedido Interactivo:** El detalle del pedido se actualiza dinámicamente a medida que se agregan artículos, calculando subtotales, impuestos (IVA, ICE) y el total general.
*   **Gestión de Usuarios:** Un formulario dedicado para administrar los usuarios del sistema, asignándolos a clientes o agentes específicos y definiendo sus roles.
*   **Integración Directa con ERP:** Al interactuar con las mismas tablas del ERP, se eliminan los silos de información y se asegura que datos críticos como el inventario, precios y estado del cliente sean siempre precisos.

---

## 📸 Galería de Pantallas

Un recorrido visual por las funcionalidades clave de la aplicación.

| Módulo de Pedidos | Búsqueda de Clientes |
| :---: | :---: |
| *Interfaz principal para la creación de pedidos.* | *Modal para buscar y seleccionar un cliente por código o nombre.* |
| ![Módulo de Pedidos](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreemPedidoBeginer.jpg) | ![Búsqueda de Clientes](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreenPedidoInProcess_01.jpg) |

| Validación de Cliente Bloqueado | Detalle de Deuda (Cuentas por Cobrar) |
| :---: | :---: |
| *El sistema notifica visualmente si un cliente está bloqueado por deudas.* | *Popup que muestra las facturas vencidas del cliente bloqueado.* |
| ![Cliente Bloqueado](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreenPedidoInProcess_02_clienteConProblemaContable.jpg) | ![Detalle de Deuda](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreenPedidoInProcess_02_clienteConProblemaContable-01.jpg) |

| Búsqueda de Artículos | Pedido en Proceso |
| :---: | :---: |
| *Selección de productos para agregar al pedido.* | *Vista de un pedido con varios artículos agregados y totales calculados.* |
| ![Búsqueda de Artículos](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreenPedidoInProcess_02_lista_articulo.jpg) | ![Pedido en Proceso](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreenPedidoInProcess_03_pedidolleno.jpg) |

| Login de Usuario | Gestión de Usuarios |
| :---: | :---: |
| *Portal de acceso seguro para los usuarios del sistema.* | *Formulario para la administración de usuarios y sus perfiles.* |
| ![Login de Usuario](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/ScreenBegin.jpg) | ![Gestión de Usuarios](https://raw.githubusercontent.com/rafaelsotove73/MVC_Sistema_Distribuidor/main/ProyectoWebMVCDistributor/Usuario.jpg) |

---

## 🛠️ Stack Tecnológico

La aplicación está construida sobre tecnologías robustas y probadas de Microsoft y la web.

*   **Plataforma y Framework:**
    *   .NET Framework 4.8
    *   ASP.NET MVC 5

*   **Backend (Controlador y Modelo):**
    *   Lenguaje: **C#**
    *   Acceso a Datos: **Entity Framework**
    *   Consultas: **LINQ (Language Integrated Query)**

*   **Frontend (Vista):**
    *   Maquetación: **HTML5** y **Razor View Engine**
    *   Estilos: **CSS3** y **Bootstrap**
    *   Interactividad: **JavaScript** y **jQuery**

*   **Base de Datos:**
    *   **Microsoft SQL Server** (Compartida con el ERP)

*   **IDE de Desarrollo:**
    *   Visual Studio 2022

---

## ⚙️ Arquitectura e Integración con ERP

El proyecto sigue una arquitectura **MVC** clásica:

1.  **Modelo:** Representa los datos de la aplicación (Clientes, Pedidos, Artículos) y la lógica de negocio. Utiliza **Entity Framework** para mapear las tablas de la base de datos del ERP a objetos C#.
2.  **Vista:** La interfaz de usuario construida con **HTML, Bootstrap y Razor**. Es responsable de presentar los datos al usuario y capturar sus interacciones.
3.  **Controlador:** Actúa como intermediario. Recibe las peticiones del usuario desde la Vista, utiliza el Modelo para consultar o manipular datos (usando **LINQ to Entities**), y devuelve la Vista apropiada.

La clave de este sistema es su **integración directa y en tiempo real con el ERP**. Al no tener una base de datos separada, se garantiza que:
*   Los estados de cuenta de los clientes están siempre actualizados.
*   Los precios y la disponibilidad de los artículos son los correctos.
*   Los pedidos generados se reflejan inmediatamente en el sistema central para su procesamiento.

---

## 🚀 Instalación y Puesta en Marcha

Para ejecutar este proyecto en un entorno de desarrollo local, sigue estos pasos:

1.  **Prerrequisitos:**
    *   Visual Studio 2022 (con la carga de trabajo "Desarrollo de ASP.NET y web").
    *   .NET Framework 4.8 Developer Pack.
    *   Acceso a una instancia de SQL Server que contenga la base de datos del ERP.

2.  **Clonar el Repositorio:**
    ```bash
    git clone https://github.com/rafaelsotove73/MVC_Sistema_Distribuidor.git
    cd MVC_Sistema_Distribuidor
    ```

3.  **Configurar la Conexión a la Base de Datos:**
    *   Abre la solución (`.sln`) en Visual Studio.
    *   Busca y abre el archivo `Web.config` en la raíz del proyecto.
    *   Localiza la sección `<connectionStrings>` y modifica la cadena de conexión para que apunte a tu instancia de SQL Server, proporcionando el servidor, nombre de la base de datos, usuario y contraseña correctos.

4.  **Restaurar Paquetes NuGet:**
    *   En el Explorador de Soluciones, haz clic derecho sobre la solución y selecciona "Restaurar paquetes NuGet".

5.  **Compilar y Ejecutar:**
    *   Presiona `F5` o haz clic en el botón "Iniciar" de Visual Studio para compilar y lanzar la aplicación en tu navegador web local.

---

## 👨‍💻 Desarrollado por

**Rafael S. Soto S.**

*   `© 2024 - ASP.NET :: Solicitud de Pedidos Vers. 1.003`
