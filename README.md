# Ghost CMS con Docker

Despliegue rápido de [Ghost](https://ghost.org/) v6 con MySQL 8 usando Docker Compose.

> Proyecto para la clase de **Ingeniería del Software** — UJCV, 2026.

## Requisitos

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) instalado y corriendo.aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

## Instalación

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/Wolfy921/CMS-Ghost.git
   cd CMS-Ghost
   ```

2. **Crear el archivo `.env`:**

   ```bash
   cp .env.example .env
   ```

   Editar `.env` con las contraseñas deseadas:

   ```
   DB_ROOT_PASSWORD=MiPasswordRoot
   DB_PASSWORD=MiPasswordGhost
   SITE_URL=http://localhost:3001
   ```

3. **Levantar los contenedores:**

   ```bash
   docker compose up -d
   ```

4. **Acceder a Ghost:**

   | Recurso | URL |
   |---|---|
   | Sitio público | [http://localhost:3001](http://localhost:3001) |
   | Panel de administración | [http://localhost:3001/ghost](http://localhost:3001/ghost) |

   La primera vez se muestra un formulario de setup para crear el usuario administrador.

## Comandos útiles

```bash
# Ver estado de los contenedores
docker compose ps

# Ver logs en tiempo real
docker compose logs -f ghost

# Detener los contenedores
docker compose down

# Detener y eliminar volúmenes (borra toda la data)
docker compose down -v
```

## Stack

| Servicio | Imagen | Puerto |
|---|---|---|
| Ghost | `ghost:6` | 3001 → 2368 |
| MySQL | `mysql:8` | interno |

## Equipo

Exposición de Ghost CMS — Ingeniería del Software, UJCV 2026.
