# **Prueba Técnica Fullstack Junior – Gestor de Notas con Autenticación**

## **Objetivo**  
Construir una aplicación web de gestor de notas donde los usuarios puedan registrarse, iniciar sesión y administrar sus notas personales.

---

## **Descripción del Proyecto**  
El usuario debe poder:  
1. **Registrarse e iniciar sesión.**  
2. **Crear notas personales.**  
3. **Ver una lista de sus notas.**  
4. **Editar o eliminar notas.**  

Cada usuario solo debe poder acceder a **sus propias notas**.  

---

## **Requisitos Técnicos**  

### **1. Frontend**  
- Usa **HTML, CSS y JavaScript** (o frameworks como **React, Vue, Angular**).  
- La interfaz debe permitir:  
  - Formulario de **registro e inicio de sesión**.  
  - Página para **crear, ver, editar y eliminar notas**.  
  - Botón para cerrar sesión.  
- El diseño debe ser limpio y responsivo.  
- Maneja errores en el frontend (por ejemplo: usuario ya registrado, credenciales incorrectas, etc.).  

---

### **2. Backend**  
- Usa **Node.js con Express**.  
- Implementa autenticación con **JWT (JSON Web Token)** para asegurar las rutas protegidas.  
- Crea los siguientes endpoints:  

| Método | Endpoint             | Descripción                         |
|--------|----------------------|-------------------------------------|
| POST   | `/auth/register`     | Registrar un nuevo usuario          |
| POST   | `/auth/login`        | Iniciar sesión                      |
| GET    | `/notes`             | Obtener todas las notas del usuario |
| POST   | `/notes`             | Crear una nueva nota                |
| PUT    | `/notes/:id`         | Actualizar una nota                 |
| DELETE | `/notes/:id`         | Eliminar una nota                   |

- Asegúrate de que los endpoints `/notes` estén protegidos y solo accesibles para usuarios autenticados.  
- Valida que los datos enviados no estén vacíos o incompletos.  

---

### **3. Base de Datos**  
- Usa **MongoDB** (o **PostgreSQL/MySQL** si prefieres).  
- Crea dos colecciones/tablas:  
   - **Usuarios**  
     - `id` (autogenerado)  
     - `username` (único)  
     - `password` (hasheado)  
   - **Notas**  
     - `id` (autogenerado)  
     - `title` (string, obligatorio)  
     - `content` (string, opcional)  
     - `userId` (referencia al usuario propietario)  

---

## **Entrega**  
1. **Código fuente:**  
   - Sube el proyecto a un repositorio en GitHub con un archivo `README.md` que explique cómo ejecutar el proyecto.  
2. **Demostración (opcional):**  
   - Despliega el proyecto en **Render, Vercel o Heroku** y proporciona el enlace.  

---

## **Criterios de Evaluación**  
1. **Autenticación:**  
   - Implementación correcta de JWT y protección de rutas.  
2. **Funcionalidad Completa:**  
   - Creación, edición y eliminación de notas funcionando correctamente.  
3. **Código Ordenado:**  
   - Claridad, organización y buenas prácticas en backend y frontend.  
4. **Interfaz de Usuario:**  
   - Diseño responsivo y fácil de usar.  
5. **Seguridad:**  
   - Hasheo de contraseñas, validación de entradas y protección de rutas.  

---

## **Tiempo Estimado**  
- **4 a 6 horas.**  
- Si necesitas más tiempo, no dudes en pedirlo.  

---

Si tienes dudas o preguntas durante la prueba, no dudes en preguntar. ¡Buena suerte y diviértete construyendo! 🚀
