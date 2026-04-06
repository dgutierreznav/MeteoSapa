# Proyecto Web Meteorológica

Este proyecto es una aplicación web para la visualización de datos meteorológicos, desarrollada con PHP y MySQL. Los datos meteorológicos incluyen temperatura, humedad, presión, velocidad del viento y precipitación. También se ha incluido un script en Python para generar datos de prueba.

---

## Miembros del proyecto

- [Oleguer Esteo](https://olegueresteo.es/)  
- [David Gutierrez](https://davidgutierrez.es/)  
- Sergi Gallart

---

## Tecnologías utilizadas

- PHP  
- MySQL  
- HTML / CSS  
- Python (para generar datos de prueba)  
- Faker (librería de Python)  
- XAMPP (Apache + MySQL + PHP)

---

## Requisitos previos

- XAMPP (o un entorno equivalente con Apache, PHP y MySQL)  
- Python 3 (para ejecutar el script de generación de datos)  
- pip (gestor de paquetes de Python)

---

## Instrucciones para poner en marcha el proyecto

1. *Instala XAMPP e inicia los servicios**:
   - Apache → Start  
   - MySQL → Start

2. **Importa la base de datos**:
   - Los scripts para crear la base de datos y las tablas se encuentran en:
     ```
     BBDD/script.sql
     ```
   - Puedes ejecutar este script con phpMyAdmin o la consola de MySQL:
     - phpMyAdmin: accede a `http://ip_servidor/phpmyadmin` e importa `BBDD/script.sql`.
     - Consola MySQL:
       ```bash
       mysql -u usuario -p nombre_base_de_datos < BBDD/script.sql
       ```

---

## Generación de datos de prueba (Python + Faker)

Se ha creado un script en Python (`aleatoriedades.py`) para generar datos de prueba automáticamente.

Características:
- Utiliza la librería `Faker`.
- Genera datos para los años 2022 a 2025.
- Por cada día se generan dos entradas diarias para cada variable meteorológica (temperatura, humedad, presión, viento y precipitación).

### Ejecutar el script de generación de datos

Es recomendable utilizar un entorno virtual Python:

1. **Crear el entorno virtual**:
   
   ```bash
   python3 -m venv venv
   ```

2. **Activar el entorno virtual**:
   - Linux / macOS:
     
     ```bash
     source venv/bin/activate
     ```
   - Windows (PowerShell):
     
     ```powershell
     .\venv\Scripts\Activate.ps1
     ```

3. **Instalar dependencias**:
   
   ```bash
   pip install faker
   ```

4. **Ejecutar el script**:
   
   ```bash
   python aleatoridades.py
   ```

5. **Desactivar el entorno virtual**:
   
   ```bash
   deactivate
   ```

---

## Acceso al proyecto

Una vez el proyecto está en funcionamiento, se puede acceder a:

- Web del proyecto:
  ```
  http://ip_servidor/Projecte/index.php
  ```

- phpMyAdmin:
  ```
  http://ip_servidor/phpmyadmin
  ```

(Sustituye `ip_servidor` por la dirección IP o `localhost` según tu entorno.)

---

## Estructura del proyecto (resum)

Árbol de archivos y carpetas principales:

```
MeteoSapa
├── /BBDD
│   └── aletoriedades.py
│   └── scripts.sql
├── /styles
│   └── styles.css
├── /imatges
│   └── fondo7.jpg
│   └── logo.png
├── /login               
│   └── login.php
│   └── login_processar.php
│   └── logout.php
│   └── registre.php
│   └── registre_processar.php
├── index.php
├── header.php
├── footer.php
├── connexio.php
├── contacte.php
├── humitat.php
├── precipitacio.php
├── preferits.php
├── preferits_afegir.php
├── preferits_eliminar.php
├── pressio.php
├── temperatura.php
└── vent.php
```

---

## Notas y recomendaciones

- Revisa `connexio.php` para configurar usuario, contraseña y nombre de la base de datos antes de ejecutar la aplicación.
- Asegúrate de que las rutas a imágenes y hojas de estilo (`/styles`, `/imatges`) sean accesibles desde el servidor Apache.

