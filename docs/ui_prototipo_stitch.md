# Documentación del Prototipo de Interfaz (UI) - SonicFlow

**Proyecto:** E-commerce de Moda Masculina  
**Versión del Prototipo:** 1.0.0  
**Herramientas:** Stitch (Diseño), HTML5, CSS3  

## 1. Descripción del Flujo
El prototipo implementado representa el **"Flujo de Compra de Usuario Registrado"**. Este recorrido cubre la experiencia completa de un cliente desde que aterriza en la tienda buscando una prenda específica, hasta que finaliza la transacción y revisa su historial.

El flujo sigue la siguiente lógica de navegación:
1.  **Exploración:** El usuario llega al **Home**, visualiza ofertas y navega al **Catálogo**.
2.  **Selección:** Filtra productos, selecciona una prenda y ve sus detalles en la **Ficha de Producto**. Añade el ítem al carrito.
3.  **Decisión:** Revisa el **Carrito de Compras** para confirmar talla y precio.
4.  **Identificación:** Al intentar pagar, el sistema solicita **Login** (si no está logueado).
5.  **Transacción:** Completa los datos de envío y pago en el **Checkout**.
6.  **Cierre:** Recibe una **Confirmación de Compra** exitosa.
7.  **Post-Compra:** Accede a su **Perfil** para verificar que la orden ha sido registrada.

---

## 2. Detalle de Pantallas

A continuación se describen las 8 pantallas diseñadas en Stitch e implementadas en HTML/CSS.

### Pantalla 01: Home (Inicio)
* **Propósito:** Captar la atención del usuario e informar sobre la identidad de marca "SonicFlow" (estilo urbano/moderno).
* **Componentes Clave:**
    * **Hero Section:** Banner de ancho completo con CTA (Call to Action) "Ver Nueva Colección".
    * **Nav Bar:** Logotipo a la izquierda, enlaces semánticos al centro, iconos de usuario/carrito a la derecha.
    * **Categorías Destacadas:** Grid de 3 columnas (Camisetas, Pantalones, Accesorios).
* **Captura:**
    * *(Inserta aquí tu imagen: `![Home Screen](./capturas/home.png)`)*

### Pantalla 02: Login (Acceso)
* **Propósito:** Permitir al usuario autenticarse o navegar hacia el registro.
* **Componentes Clave:**
    * Formulario centrado con validación visual básica.
    * Inputs semánticos (`type="email"`, `type="password"`).
    * Enlace "¿Olvidaste tu contraseña?".
* **Captura:**
    * *(Inserta aquí tu imagen: `![Login Screen](./capturas/login.png)`)*

### Pantalla 03: Catálogo (Listado de Productos)
* **Propósito:** Mostrar la oferta de productos disponible con opciones de filtrado.
* **Componentes Clave:**
    * **Sidebar (Aside):** Filtros por precio, talla y color.
    * **Grid Principal:** Diseño responsivo (CSS Grid) que muestra tarjetas de producto.
    * **Card de Producto:** Imagen, Nombre, Precio y botón rápido de "Ver detalles".
* **Captura:**
    * *(Inserta aquí tu imagen: `![Catalogo Screen](./capturas/catalogo.png)`)*

### Pantalla 04: Detalle de Producto
* **Propósito:** Proveer información específica para la toma de decisión de compra.
* **Componentes Clave:**
    * Contenedor Flexbox de dos columnas (Escritorio).
    * Selector de Talla (S/M/L) usando elementos `<select>` o `<input type="radio">`.
    * Botón prominente "Añadir al Carrito".
* **Captura:**
    * *(Inserta aquí tu imagen: `![Detalle Screen](./capturas/producto.png)`)*

### Pantalla 05: Carrito (Resumen)
* **Propósito:** Permitir al usuario gestionar los items antes de pagar.
* **Componentes Clave:**
    * Tabla semántica o lista de items con miniaturas.
    * Controles de cantidad (+/-).
    * Panel lateral de "Resumen del Pedido" (Subtotal, Envío, Total).
* **Captura:**
    * *(Inserta aquí tu imagen: `![Carrito Screen](./capturas/carrito.png)`)*

### Pantalla 06: Checkout (Pasarela)
* **Propósito:** Recolectar datos finales de envío y facturación.
* **Componentes Clave:**
    * Formulario multipartes (Datos de Envío / Método de Pago).
    * Uso de `<fieldset>` y `<legend>` para agrupar secciones del formulario.
    * Resumen estático de la compra visible durante el proceso.
* **Captura:**
    * *(Inserta aquí tu imagen: `![Checkout Screen](./capturas/checkout.png)`)*

### Pantalla 07: Confirmación (Éxito)
* **Propósito:** Dar feedback positivo inmediato al usuario y proporcionar el número de seguimiento.
* **Componentes Clave:**
    * Icono de estado "Success/Check".
    * Número de Orden generado.
    * Botón secundario "Volver a la tienda".
* **Captura:**
    * *(Inserta aquí tu imagen: `![Confirmacion Screen](./capturas/confirmacion.png)`)*

### Pantalla 08: Perfil de Usuario
* **Propósito:** Espacio personal para gestionar datos e historial.
* **Componentes Clave:**
    * Menú lateral de navegación del perfil (Datos, Pedidos, Direcciones).
    * Tabla de "Historial de Pedidos" mostrando estado (Enviado, Pendiente).
* **Captura:**
    * *(Inserta aquí tu imagen: `![Perfil Screen](./capturas/perfil.png)`)*

---

## 3. Aspectos Técnicos

### Maquetación Semántica
Se ha priorizado el uso de etiquetas HTML5 para garantizar la estructura lógica del documento:
* `<header>` y `<footer>` en todas las páginas.
* `<nav>` para menús de navegación.
* `<main>` para el contenido principal único de cada vista.
* `<article>` para las tarjetas de producto en el catálogo.
* `<aside>` para las barras laterales de filtros.

### Diseño Responsivo
La interfaz se adapta a dispositivos móviles y escritorio mediante:
* **CSS Grid:** Utilizado en el catálogo (`grid-template-columns: repeat(auto-fill, minmax(250px, 1fr))`) para reacomodar tarjetas automáticamente.
* **Flexbox:** Utilizado en el Header y Footer para alineación de elementos.
* **Media Queries:** Breakpoints en `768px` para transformar menús horizontales en verticales en dispositivos móviles.

### Criterios de Accesibilidad
* Contraste de colores verificado para legibilidad (Texto oscuro sobre fondo claro).
* Atributos `alt` descriptivos en todas las imágenes de productos.
* Etiquetas `<label>` correctamente vinculadas a sus inputs mediante el atributo `for`.