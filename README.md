# 🚀 Projecte: Montsià 30 - Migració a WordPress


## 📋 Requisits Previs de l'Entorn (Servidor)

Per poder executar aquesta pràctica i utilitzar l'eina de migració correctament, el servidor (màquina virtual) ha de complir els següents requisits:

### 1. Infraestructura
* **Sistema Operatiu:** Màquina virtual Linux accessible via xarxa (ex: `192.168.32.129`).
* **Docker i Docker Compose:** Instal·lats i funcionant per poder aixecar els contenidors de WordPress i la base de dades (MariaDB/MySQL).

### 2. Configuració de WordPress
L'entorn de WordPress ha d'estar operatiu pel port `8080` i ha de tenir instal·lats i actius els següents **Plugins**:
* `JWT Authentication for WP REST API` (Obligatori per a l'autenticació del migrador).
* `WP API SwaggerUI` (Per comprovar i testejar els endpoints de l'API).
* `File Manager` (Per a la gestió d'arxius interna des del panell).
* `Blank Slate` amb el tema `Hello Elementor` (Per evitar conflictes d'estils amb l'HTML migrat).
