# Servicio Web RESTful con Flask y JSON

Proyecto académico de backend desarrollado con **Flask**, usando el estilo **RESTful** y respuestas en **JSON**. Está preparado para ser probado con Postman, Thunder Client o consumido desde una aplicación móvil en Flutter.

## 1. Características

- Framework: Flask.
- Formato de intercambio: JSON.
- Base de datos: SQLite.
- ORM: Flask-SQLAlchemy.
- CORS habilitado para consumo desde Flutter u otros clientes.
- Autenticación con JWT.
- Arquitectura por capas tipo MVC:
  - `models`: entidades de base de datos.
  - `repositories`: acceso a datos.
  - `services`: lógica de negocio.
  - `controllers`: control de solicitudes y respuestas.
  - `routes`: definición de endpoints.

## 2. Estructura del proyecto

```text
flask_restful_json_service/
│
├── app/
│   ├── controllers/
│   │   ├── auth_controller.py
│   │   └── producto_controller.py
│   ├── models/
│   │   ├── usuario_model.py
│   │   └── producto_model.py
│   ├── repositories/
│   │   ├── usuario_repository.py
│   │   └── producto_repository.py
│   ├── routes/
│   │   ├── auth_routes.py
│   │   └── producto_routes.py
│   ├── services/
│   │   ├── auth_service.py
│   │   └── producto_service.py
│   ├── utils/
│   │   └── seed.py
│   ├── config.py
│   ├── extensions.py
│   └── __init__.py
│
├── run.py
├── requirements.txt
├── test_api.http
├── .env.example
└── README.md
```

## 3. Instalación en Windows

```bash
cd flask_restful_json_service
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
python run.py
```

## 4. Instalación en Linux o macOS

```bash
cd flask_restful_json_service
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
python run.py
```

## 5. URL base

```text
http://localhost:5000
```

Para emulador Android de Flutter:

```dart
const String baseUrl = 'http://10.0.2.2:5000/api';
```

Para celular físico, reemplazar `localhost` o `10.0.2.2` por la IP local de la computadora donde se ejecuta Flask.

## 6. Usuario de prueba

```text
Usuario: admin
Clave: 123456
```