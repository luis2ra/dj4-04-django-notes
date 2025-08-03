# Django Notes

Una aplicación web de notas desarrollada con Django 4.2.4.

**Nota**: Tomado como referencia del canal Fatz

Link: [Django CRUD con Autenticacion y Despliegue Gratuito (Login,Register, Rutas protegidas, y mas)](https://www.youtube.com/watch?v=e6PkGDH4wWA)

## 🚀 Configuración del Entorno

Este proyecto puede configurarse de dos maneras:

### Opción 1: Con pyenv (Recomendado si tienes pyenv)

El archivo `.python-version` contiene `django4`, que indica el entorno original.

```bash
# Instalar pyenv si no lo tienes
curl https://pyenv.run | bash

# Crear el entorno django4 con Python 3.11.13 (LTS)
pyenv install 3.11.13
pyenv virtualenv 3.11.13 django4
pyenv local django4

# Instalar dependencias
pip install -r requirements.txt
```

### Opción 2: Con venv (Más simple)

```bash
# Crear entorno virtual
python3 -m venv venv

# Activar entorno
source venv/bin/activate

# Instalar dependencias
pip install -r requirements.txt
```

## 🏃‍♂️ Ejecutar el proyecto

```bash
# Activar entorno (solo si usas venv)
source venv/bin/activate

# Ejecutar migraciones (si es necesario)
python manage.py migrate

# Iniciar servidor
python manage.py runserver
```

## 📦 Dependencias

- Django 4.2.4
- asgiref
- autopep8
- pycodestyle
- sqlparse
- toml

## 📁 Estructura del proyecto

```
djangocrud/          # Configuración principal
tasks/              # App de tareas/notas
├── templates/      # Plantillas HTML
├── migrations/     # Migraciones de DB
└── ...
```

## 🗄️ Base de datos

El proyecto usa SQLite (`db.sqlite3`) que se incluye para facilitar el setup inicial.

---

**Nota**: El archivo `.python-version` indica el setup original con pyenv, pero puedes usar venv si prefieres simplicidad.
