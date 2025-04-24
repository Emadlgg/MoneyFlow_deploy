# 💰 MoneyFlow - Entorno de Despliegue

## 🐳 Configuración con Docker Compose

### ✅ Requisitos
- Docker 20.10+
- Docker Compose 2.0+

### 🔧 Instalación
```bash
git clone https://github.com/tu-org/moneyflow-deploy.git
git clone https://github.com/tu-org/moneyflow-backend.git ../moneyflow-backend
git clone https://github.com/tu-org/moneyflow-frontend.git ../moneyflow-frontend
docker-compose up --build
```

## 🧩 Servicios

| Servicio   | Puerto | URL                         |
|------------|--------|-----------------------------|
| Frontend   | 3001   | http://localhost:3001       |
| Backend    | 3000   | http://localhost:3000       |
| PostgreSQL | 5432   | postgres://db:5432          |

## 🔁 Comandos Clave
```bash
# Levantar servicios en segundo plano
docker-compose up -d

# Ver logs
docker-compose logs -f

# Reconstruir imágenes
docker-compose build --no-cache
```

## 🔐 Variables de Entorno
Configurar en los respectivos repositorios:
- `moneyflow-backend/.env`
- `moneyflow-frontend/.env`

## 📦 Estructura del Proyecto
```bash
.
├── docker-compose.yml   # Orquestación completa
└── scripts/             # Utilidades de despliegue
```

> ✨ Nota: Para desarrollo local con hot-reload, ejecutar los servicios directamente en cada repositorio correspondiente.
