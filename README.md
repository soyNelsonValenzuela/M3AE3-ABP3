# Proyecto EcoRuta – M3AE3 ABP3

Este proyecto corresponde a la actividad **"Diseño modular de estilos con SASS usando el patrón 7-1"** del módulo 3. Su objetivo es construir la interfaz web de la empresa ficticia EcoRuta aplicando buenas prácticas de organización y modularización de estilos en SASS para lograr una experiencia clara, escalable y fácil de mantener.

## 🎯 Aprendizaje Esperado

> Aplicar el patrón 7-1 en SASS para estructurar parciales de estilos, crear componentes reutilizables y garantizar la mantenibilidad de un proyecto frontend real. ```


# Descripción del proyecto

EcoRuta es una interfaz web modular construída con HTML, CSS y SASS siguiendo el patrón 7-1. Permite a los usuarios planificar rutas ecológicas —a pie, en bici o transporte público—, obtener puntos por trayectos verdes y consultar un blog de vida sustentable.

---

## 📁 Estructura del proyecto

```
M3AE3-ABP3/
├── assets/
│   # Imágenes (logo, hero, etc.)
├── css/
│   ├── sass/
│   │   ├── _variables.scss
│   │   ├── _mixins.scss
│   │   ├── _functions.scss
│   │   ├── _reset.scss
│   │   ├── _typography.scss
│   │   ├── _colors.scss
│   │   ├── _buttons.scss
│   │   ├── _cards.scss
│   │   ├── _header.scss
│   │   ├── _footer.scss
│   │   └── _hero.scss
│   ├── style.scss            # Archivo principal (importa todos los parciales)
│   └── style.css             # Generado por SASS
├── html/
│   └── index.html            # Página principal
└── package.json              # Dependencias y scripts
```

---

## 🚀 Instalación

1. **Clonar el repositorio**  
   ```bash
   git clone https://github.com/soyNelsonValenzuela/M3AE3-ABP3.git
   cd M3AE3-ABP3
   ```

2. **Instalar dependencias**  
   ```bash
   npm install
   ```

   Esto descargará SASS (y cualquier otro módulo) definido en `package.json`.

3. **Compilar SASS a CSS**  
   - **Una sola vez**:  
     ```bash
     npm run build-css
     ```
   - **Modo “watch”** (recompila al detectar cambios):  
     ```bash
     npm run watch-css
     ```

   > Estos scripts vienen pre-configurados en `package.json`:
   > ```json
   > {
   >   "scripts": {
   >     "build-css": "sass css/style.scss css/style.css",
   >     "watch-css": "sass --watch css/style.scss css/style.css"
   >   },
   >   "devDependencies": {
   >     "sass": "^1.x"
   >   }
   > }
   > ```

---

## ⚙️ Uso

1. Tras compilar, abre `html/index.html` en tu navegador.
2. El header está fijo en la parte superior.
3. La sección **Hero** muestra un título, párrafos e imagen responsiva.
4. La sección **Servicios** usa tarjetas reutilizables (`.card`).
5. El footer incluye enlaces a redes sociales con íconos de Font Awesome.

---

## 🛠 Tecnologías

- **HTML5**  
- **SASS** (patrón 7-1 con parciales)  
- **CSS3** (compilado desde SASS)  
- **Font Awesome** para íconos  
- **npm & SASS CLI** para compilación  

---

## 📖 Cómo está organizado SASS (patrón 7-1)

1. **_variables.scss**Espaciados, radios…  
2. **_mixins.scss**: Mixins para media queries.
3. **_functions.scss**: Funciones personalizadas (opcional).  
4. **_reset.scss**: Reset básico de estilos.  
5. **_typography.scss**: Tipografía global y enlaces.  
6. **_components**:  
   - _buttons.scss  
   - _cards.scss  
7. **_layout**:  
   - _header.scss  
   - _footer.scss
8. **_colors.scss**: Colores base.


El `style.scss` importa todos los parciales con `@use`, produciendo un único `style.css` para el navegador.

---

## 🧑‍💻 Autor

**Nelson Valenzuela Gómez**

---