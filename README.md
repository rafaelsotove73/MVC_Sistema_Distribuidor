Sistema de Pedidos para Distribuidores (MVC_Sistema_Distribuidor)
![alt text](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=dotnet&logoColor=white)

![alt text](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)

![alt text](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)

![alt text](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

![alt text](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
Sistema web para la gestión de solicitudes de pedidos para distribuidores, desarrollado con el patrón ASP.NET MVC. La aplicación se integra directamente con un ERP existente para la validación de datos en tiempo real y la grabación de transacciones.
Descripción General
Este proyecto, bajo el nombre METALTRONIC GROUP :: APLICACION WEB, tiene como objetivo principal proporcionar a los distribuidores una plataforma web para autogestionar sus solicitudes de pedidos. La aplicación agiliza el proceso de compra, valida la información del cliente contra el sistema central (ERP) y permite registrar los pedidos directamente en la base de datos de la empresa.
Flujo de Trabajo de la Aplicación
El flujo principal de la aplicación, como se muestra en las capturas de pantalla, es el siguiente:
Autenticación: El usuario (agente o distribuidor) inicia sesión a través de un formulario de login.
Gestión de Usuarios (Admin): Existe un módulo para la administración de usuarios, donde se pueden crear, editar y asociar usuarios de la aplicación con códigos de Cliente y Agente del ERP.
Inicio del Módulo de Pedidos: El usuario accede al módulo "Solicitud Pedido Distribuidor".
Búsqueda y Selección de Cliente: El usuario busca un cliente por código o nombre. El sistema muestra una lista de coincidencias.
Validación de Cliente: Al seleccionar un cliente, la aplicación consulta en tiempo real el ERP para:
Verificar el cupo de crédito disponible.
Comprobar si el cliente está bloqueado por facturas vencidas u otras razones. Si está bloqueado, se muestra una alerta y los detalles de la deuda.
Búsqueda de Artículos: El usuario puede buscar productos por modelo, color u otros criterios.
Creación del Pedido: Los artículos seleccionados se añaden a un carrito de "Detalles del Pedido", donde se puede ajustar la cantidad. El sistema calcula automáticamente los subtotales, IVA y el total general.
Grabación del Pedido: Una vez completado, el pedido se graba directamente en las tablas del ERP, generando una nueva solicitud.
Características Principales
Arquitectura MVC: Separación clara de responsabilidades (Modelo, Vista, Controlador).
Integración con ERP: Conexión directa a la base de datos de un ERP para leer datos de clientes, productos y estado financiero, y para escribir los nuevos pedidos.
Validación en Tiempo Real: Comprobación instantánea del estado del cliente (bloqueado/activo) y su línea de crédito.
Interfaz Responsiva: Uso de Bootstrap para una experiencia de usuario adaptable a diferentes dispositivos.
Búsquedas Asíncronas: Funcionalidades de búsqueda que no requieren recargar la página completa, mejorando la experiencia de usuario.
Módulo de Administración: Gestión de los usuarios que pueden acceder al sistema.
Pila Tecnológica (Stack)
Backend: C#
-- Framework: ASP.NET MVC 5
Frontend:
HTML5
CSS3
Bootstrap
Razor View Engine
JavaScript / jQuery (para la interactividad)
Base de Datos: Microsoft SQL Server
Entorno de Desarrollo: Visual Studio 2022
Arquitectura de Integración con ERP
Una característica clave de esta aplicación es su integración directa con un sistema ERP. La aplicación no solo lee datos (como clientes, artículos, precios y estado de cuenta), sino que también escribe directamente en las tablas del ERP para registrar las solicitudes de pedido.
Esto elimina la necesidad de procesos de importación/exportación manuales, asegurando que la información esté centralizada y actualizada al instante.
Lectura: Clientes, Articulos, FacturasPorCobrar, Vendedores, ListasDePrecios.
Escritura: CabeceraDePedidos, DetalleDePedidos.
