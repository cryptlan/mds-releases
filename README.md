# mds-releases

Huellas publicadas de cada versión de **Mi Diario de Salud** (https://mds.cryptlan.com).

Aquí solo hay manifiestos: ni código ni datos de nadie. Cada vez que se publica una versión se añade `releases/<versión>.json` con la versión, el commit, la fecha de construcción (UTC) y, para cada fichero que sirve la aplicación, su ruta y su huella SHA-256.

El historial no se puede reescribir: la rama `main` no admite *force push* ni borrado. Cualquier versión servida queda registrada aquí con fecha pública.

## Cómo comprobar una versión

1. Mira qué versión sirve la app: https://mds.cryptlan.com/version.json
2. Abre aquí `releases/<esa versión>.json`.
3. Descarga cualquier fichero de la lista desde `https://mds.cryptlan.com/<ruta>` y calcula su SHA-256:
   - Windows (PowerShell): `Get-FileHash .\fichero -Algorithm SHA256`
   - Linux/macOS: `sha256sum fichero`
4. La huella debe coincidir con la del manifiesto. Si no coincide, o si la versión servida no aparece aquí, se está sirviendo algo no publicado.

Nota: el navegador puede guardar en caché una versión anterior; para comprobar, descarga los ficheros directamente.

Esto prueba qué ficheros se sirven, no que el código sea correcto.
