# PokeDex — Despliegue en Azure App
### Seguridad
Se agregaron los encabezados HTTP de seguridad en un web.config
#### Headers: 
- Content-Security-Policy 
- Strict-Transport-Security
- X-Content-Type-Options
- X-Frame-Options
- Referrer-Policy
- Permissions-Policy

### Creación del Web App 

| Detalles | |
|---|---|
| Resource Group| rg-pokedex-prod |
| Name | web-pokedex-app |
| Tarjeta de crédito requerida | No |
| Runtime Stack | Node.js 22 |
---

| App Service Plan | |
|---|---|
| Operating System| Windows |
| Region| Brazil South |
| SKU | Free |
| Runtime Stack | Node.js 22 |
---

## Comandos de despliegue
1. Subida de archivo zip del dist
3. Descomprimir Archivo: **powershell -command "Add-Type -Assembly System.IO.Compression.FileSystem; [System.IO.Compression.ZipFile]::ExtractToDirectory('C:\home\site\wwwroot\deploy.zip', 'C:\home\site\wwwroot'**

## Ejecución en el Local
1.  Descarga del proyecto
2. **npm install**
3. **npm start** 
4. **npm run build** - Generó el dist

**IMPORTANTE:** Tuve que cambiar de versión de Node.Js de 23 a 22. Al hacer **npm run build** parecia un build eterno, con la versión 22 no tardó ni 1 minuto.
