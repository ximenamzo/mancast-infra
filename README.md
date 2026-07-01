# mancast-infra
docker-compose.yml raíz, documentación general, diagramas

Repositorio de infraestructura y documentación del proyecto **ManCast**, un sistema
de gestión y distribución multi-sucursal construido con Laravel, Angular y .NET Core.

Este repo **no contiene lógica de negocio**. Su propósito es orquestar los demás
servicios y centralizar la documentación del proyecto.

## Repos del proyecto

| Repo | Responsabilidad |
|---|---|
| [mancast-laravel-api](../mancast-laravel-api) | Productos, clientes, autenticación |
| [mancast-dotnet-api](../mancast-dotnet-api) | Traslados entre sucursales, cálculos de costo |
| [mancast-angular](../mancast-angular) | Frontend |

## Estructura local

```
ManCast/
├── mancast-infra/          <- este repo
├── mancast-laravel-api/
├── mancast-dotnet-api/
└── mancast-angular/
```

Los cuatro repos deben clonarse como carpetas hermanas dentro de `ManCast/` para que
las rutas relativas del `docker-compose.yml` (`../mancast-laravel-api`, etc.) funcionen.

## Cómo levantar el entorno

```bash
docker compose up -d
docker compose ps
```

## Documentación

- [REQUIREMENTS.md](./REQUIREMENTS.md) — requerimientos funcionales y no funcionales, modelo de datos preliminar


