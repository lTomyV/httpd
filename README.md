# Publicar archivos en Apache HTTPD usando Docker

Este proyecto muestra cómo publicar archivos estáticos de un directorio local utilizando Apache HTTPD en Docker, en el puerto 8090.

## Requisitos

- Docker Desktop instalado

## Instrucciones

1. Clonar el repositorio (o descargarlo).
2. Asegurarse de que haya archivos en `mi_sitio_web` (hay un `index.html` de ejemplo).
3. Ejecutar en PowerShell o CMD, desde la carpeta `httpd`:

```powershell
docker run -d `
  --name mi_apache `
  -p 8090:80 `
  -v ${PWD}\mi_sitio_web:/usr/local/apache2/htdocs/ `
  httpd
