# ServitechWeb

Plataforma web para conectar usuarios con expertos en informática.

## Estructura del proyecto

```
servitech/
│
├── backend/    # Node.js + Express + MongoDB (API REST)
│   ├── src/
│   ├── package.json
│   └── ...
│
├── views/   # HTML, CSS, JS (interfaz de usuario)
│   ├── index.html
│   ├── assets/
│   └── ...
│
├── README.md
└── .gitignore
```

## Instalación y ejecución

### Requisitos

- Node.js y npm
- MongoDB (local o Atlas)

### Paso a paso para inicializar el proyecto

1. **Clona el repositorio**

   ```bash
   git clone https://github.com/DianaJJ0/servitechWeb.git
   cd servitechWeb
   ```

2. **Configura el backend**

   ```bash
   cd backend
   npm install
   ```

3. **Configura las variables de entorno**

   - Copia el archivo `.env.example` a `.env`:
     ```bash
     cp .env.example .env
     ```
   - Edita el archivo `.env` y asegúrate de definir:
     ```
     MONGODB_URI=mongodb://localhost:27017/servitech
     PORT=3000
     JWT_CONTRASEÑA=tu_clave_secreta
     ```

4. **Inicia MongoDB**

   - Si usas MongoDB local, abre una terminal nueva y ejecuta:
     ```bash
     mongod
     ```
   - Si usas MongoDB Atlas, asegúrate de que tu URI esté correctamente configurada en `.env`.

5. **Inicia el backend**

   ```bash
   cd backend
   node src/app.js
   ```
   > **Nota:** Debes ejecutar este comando **dentro de la carpeta `backend`**.  
   > No lo ejecutes desde la carpeta `views`, porque ahí no existe el archivo `src/app.js`.

6. **Abre el views (ahora usando EJS y Express)**

   - Abre tu navegador y accede a:  
     ```
     http://localhost:3000/
     ```
   - Para otras páginas, usa rutas como:  
     ```
     http://localhost:3000/mis-asesorias.html
     http://localhost:3000/expertos.html
     http://localhost:3000/registro.html
     ```

---

## Funcionalidades principales

- Registro y login de usuarios (con JWT)
- Gestión de usuarios y expertos
- Conexión a MongoDB para almacenamiento de datos
- Interfaz moderna y responsiva

---

## Notas

- No subas tu archivo `.env` real al repositorio.
- Puedes ver y administrar los datos con MongoDB Compass.

---

## Autor

~ Diana Carolina Jimenez ~

---
