# Mi Primera API con FastAPI

Una API REST básica desarrollada con **FastAPI**, uno de los frameworks más rápidos y modernos para construir aplicaciones web y APIs en Python.

## Descripción

Este proyecto implementa un endpoint simple que devuelve un mensaje de bienvenida cuando se accede a la ruta principal (`/`).

### Respuesta esperada

```json
{
  "message": "¡Hola, Fast API!"
}
```

---

## Tecnologías utilizadas

* Python 3.x
* FastAPI
* Uvicorn

---

## Estructura del proyecto

```text
.
├── main.py
└── README.md
```

---

## Código fuente

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "¡Hola, Fast API!"}
```

---

## Instalación

### 1. Crear un entorno virtual (opcional)

```bash
python -m venv venv
```

### 2. Activar el entorno virtual

Windows:

```bash
venv\Scripts\activate
```

Linux / macOS:

```bash
source venv/bin/activate
```

### 3. Instalar dependencias

```bash
pip install fastapi uvicorn
```

---

## Ejecutar la aplicación

```bash
uvicorn main:app --reload
```

La API estará disponible en:

```text
http://127.0.0.1:8000
```

---

## Documentación automática

FastAPI genera documentación interactiva automáticamente.

### Swagger UI

```text
http://127.0.0.1:8000/docs
```

### ReDoc

```text
http://127.0.0.1:8000/redoc
```

---

## Endpoint disponible

| Método | Ruta | Descripción                      |
| ------ | ---- | -------------------------------- |
| GET    | /    | Retorna un mensaje de bienvenida |

---

## Resultado

Al realizar una petición GET a la ruta principal:

```bash
GET /
```

Se obtiene:

```json
{
  "message": "¡Hola, Fast API!"
}
```

---

## Autor

Proyecto desarrollado como práctica introductoria al framework FastAPI para la creación de APIs modernas con Python.
