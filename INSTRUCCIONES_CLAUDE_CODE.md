# Instrucciones para Claude Code

Este proyecto necesita ser publicado como un nuevo repositorio en GitHub con GitHub Pages activado.

## Tarea

1. **Crear un repositorio nuevo público** en GitHub llamado `desafio-robotica-2026` bajo la cuenta del usuario `ffrumej917`.

2. **Subir todo el contenido de esta carpeta** al repositorio:
   - `index.html` (página principal)
   - `README.md`
   - `.gitignore`
   - Carpeta `1ESO/` completa
   - Carpeta `2ESO/` (vacía por ahora pero con `.gitkeep` si GitHub la descarta)
   - Carpeta `docs/` completa
   - Carpeta `assets/` (vacía por ahora)

3. **Activar GitHub Pages** desde la rama `main`, carpeta raíz (`/`).

4. **Verificar** que la URL pública funciona: `https://ffrumej917.github.io/desafio-robotica-2026/`

## Comandos sugeridos

Si prefieres hacerlo por terminal con `gh` CLI:

```bash
cd desafio-robotica-2026
git init
git add .
git commit -m "Initial commit: estructura base + S01 de 1º ESO"
gh repo create ffrumej917/desafio-robotica-2026 --public --source=. --remote=origin --push
gh api -X POST /repos/ffrumej917/desafio-robotica-2026/pages \
  -f source='{"branch":"main","path":"/"}'
```

## Notas importantes

- **Carpetas vacías**: Git no sube carpetas vacías. Si `2ESO/` o `assets/` tienen que mantenerse, añade un archivo `.gitkeep` vacío dentro de cada una antes del primer commit.

- **Nombres de archivos con tildes o espacios**: GitHub los soporta pero pueden dar problemas en URLs. En esta estructura todos los nombres usan kebab-case y no tienen tildes, por lo que no debería haber problema.

- **Ficha .docx**: Se sirve como descarga directa desde GitHub Pages. No es ideal que esté en el repo (binario), pero mientras no ocupe mucho es aceptable.

- **Tras el primer despliegue**: GitHub Pages tarda 1-2 minutos en propagar cambios. Si la URL no responde inmediatamente, esperar.

## Actualización futura

Cuando el profesor Fabi añada nuevas sesiones, el flujo será:

```bash
# Copiar los archivos nuevos a la carpeta correspondiente (1ESO/S02-.../ o 2ESO/S01-.../)
# Actualizar index.html cambiando <span class="btn-link disabled">Próximamente</span>
# por los botones con enlaces reales
git add .
git commit -m "Añadir S02 de 1º ESO: el sprite reactivo"
git push
```
