# Guía de Despliegue en Firebase Hosting (Mr. Pitti's)

Para subir tu sitio directamente a Firebase Hosting sin activar Firestore u otros servicios adicionales, sigue estos pasos desde tu terminal (PowerShell o CMD):

## 1. Instalación de Herramientas
Si aún no tienes las herramientas de Firebase, instálalas globalmente con Node.js:
```powershell
npm install -g firebase-tools
```

## 2. Inicio de Sesión
Inicia sesión con tu cuenta de Google asociada a Firebase:
```powershell
firebase login
```

## 3. Inicialización del Proyecto
Desde la carpeta raíz del proyecto (`mr-pittis-web`), ejecuta:
```powershell
firebase init hosting
```

### Configuración recomendada durante el init:
1. **Select Project:** Elige "Use an existing project" y selecciona tu proyecto de **Firebase Studio**.
2. **Public Directory:** Escribe `.` (esto indica que el directorio actual, donde está tu `index.html`, es la raíz).
3. **Single Page App:** Elige `N` (No).
4. **File Overwrite:** Si te pregunta por sobreescribir `index.html`, elige **No**.

## 4. Despliegue Directo
Una vez inicializado, solo necesitas este comando para actualizar el sitio:
```powershell
firebase deploy --only hosting
```

---
> [!TIP]
> Al usar Hosting independiente, solo pagas/consumes por el ancho de banda y almacenamiento de archivos estáticos (el video es el que más consumirá, por eso habilitamos el lazy-loading).
