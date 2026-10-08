# Sistema Escolar - Control de Acceso y Captura de Usuarios

---

## 📋 Portada

* **Institución:** Instituto Tecnológico de Oaxaca
* **Asignatura:** Programación Web
* **Proyecto:** Sistema Escolar (Login + Panel Principal)
* **Integrantes del Equipo:**
  * Carlos Enrique García Unda (23160911)
  * Uriel Eduardo Guzmán Ramírez
* **Enlace al Repositorio:** [https://github.com/CarlosEnriqueGarciaUnda/Actividad5](https://github.com/CarlosEnriqueGarciaUnda/Actividad5Equipo)
* **Enlace a GitHub Pages:** [https://CarlosEnriqueGarciaUnda.github.io/Actividad5/login.html](https://carlosenriquegarciaunda.github.io/Actividad5Equipo/login.html)

---

## 📝 Descripción Breve del Proyecto

Este proyecto consiste en una aplicación web interactiva formada por dos vistas principales interconectadas:
1. **`login.html`**: Pantalla de autenticación de usuario con validación de credenciales en tiempo real en el cliente.
2. **`index.html`**: Panel principal del sistema escolar que cuenta con navegación mediante barra superior (*Navbar*), menú lateral desplegable (*Sidebar*), formularios de captura validados y cálculo dinámico de edad mediante una ventana modal.

---

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructuración semántica de las vistas web.
* **CSS3 Custom:** Hojas de estilo personalizadas para ajustes visuales específicos.
* **Bootstrap v5.3.3:** Framework de diseño responsivo utilizado para componentes como tarjetas, barras de navegación, acordeones, cuadrículas y modales.
* **JavaScript (ES6):** Manipulación del DOM, gestión de eventos y consumo de métodos de validación.

---

## 🔄 Explicación Técnica y Flujo de Datos

### 1. Flujo del Login al Sistema
El proceso de inicio de sesión no requiere de un servidor backend, sino que simula la sesión a través del navegador:
1. El usuario ingresa su correo electrónico y contraseña en `login.html`.
2. Al presionar "Iniciar sesión", JavaScript captura el evento `submit` e interrumpe el envío por defecto con `event.preventDefault()`.
3. Se evalúan los datos utilizando las funciones `validarCorreo()` y `validarPassword()` de la librería `utileria.js`.
4. Si los datos son válidos, el valor del correo ingresado se almacena en el almacenamiento local del navegador mediante:
   ```javascript
   localStorage.setItem("usuarioLogueado", correoIngresado);
