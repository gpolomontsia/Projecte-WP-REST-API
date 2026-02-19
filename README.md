# Projecte SPRINT2 - Migració a WordPress
Aquesta és una guia pràctica per realitzar el procés de migració del projecte SPRINT1 (fet amb codi vanilla) a un WordPress dockeritzat dins d'un Ubuntu Server mitjançant JavaScript i WP REST API.
<br><br>

## Requisits Previs
Per tal de realitzar aquesta practica correctament, s'han de tenir com a mínim els següents requisits previs:
* Màquina virtual **Ubuntu Server** (24.04 LTS preferiblement) accessible des de la xarxa (en aquest cas, des de 192.168.32.129).
* Servei **docker.io** (paquet lleuger de docker) instal·lat amb **docker-compose**.
* Ganes d'aprendre i calentar-se el cap programant JS sense utilitzar Gemini Pro.
<br>

## 1. Desplegament amb Docker

Crearem una carpeta anomenada **projecte_wordpress** i dins d'aquesta l'arxiu **docker-compose.yml**, on afegirem els contenidors per a **WordPress** i **MariaDB** amb els seus respectius volums:

<img width="313" height="523" alt="docker-compose" src="https://github.com/user-attachments/assets/17ba7307-f132-49b1-a239-618d85008f94" />
<br><br>

Després d'executar **docker-compose up -d**, ja podrem accedir a **WordPress** des del navegador web inserint **192.168.32.169:8080**.
<br><br>

## 2. Configuració de WordPress

Dins del panell d'administració de **WordPress**, crearem un usuari amb **Perfil Editor** amb el que ens autenticarem posteriorment:

<img width="550" alt="usuari-editor" src="https://github.com/user-attachments/assets/a29ea406-015b-45b8-884d-7b28b56cb2c8" />
<br><br>

Per configurar els arxius de WordPress des d'interfície gràfica, instal·larem el plugin **File Manager** (opcional):

<img width="550" alt="plugin-file-manager" src="https://github.com/user-attachments/assets/b0166d70-5f56-4204-b153-f4a36b349cb6" />
<br><br>

Per realitzar l'autenticació de la **WP REST API** mitjançant el mètode **JWT** (JSON Web Tokens), haurem d'instal·lar el plugin **JWT Authentication for WP REST API**:

<img width="550" alt="plugin-jwt" src="https://github.com/user-attachments/assets/d9584439-104d-4a85-b8c5-c77d3e1e011f" />
<br><br>

Dins de la configuració d'aquest Plugin, veurem que ens demana afegir dues línies (utilitzant CORS Support) dins de l'arxiu **wp-config.php** per habilitar l'autenticació amb **JWT**:

<img width="550" alt="Configuracio-JWT" src="https://github.com/user-attachments/assets/95f902d6-1047-4472-8108-c8a05ed9423a" />
<br><br>

Aprofitarem l'explorador d'arxius instal·lat anteriorment per editar l'arxiu **wp-config.php**:

<img width="600" alt="explorador-arxius" src="https://github.com/user-attachments/assets/21f87bd5-75a7-4ea6-b002-48dbb6dfc767" />
<br><br>

Dins d'aquest, inserirem les línies de configuració de **JWT** just abans del comentari _That's all, stop editing!_:

<img width="550" alt="edicio-wp-config" src="https://github.com/user-attachments/assets/e446de06-f068-4b3a-887d-ca869613cc4d" />
<br><br>

Amb aquesta configuració bàsica, ja haurem deixat WordPress llest per rebre peticions externes mitjançant **WP REST API**
<br><br>

## 3. Connexió amb Fetch API

Utilitzarem el codi de l'arxiu **get-posts.html** proporcionat dins del repositori per comprovar que **WordPress** accepta peticions externes:

<img width="500" alt="get-posts" src="https://github.com/user-attachments/assets/d18cf527-2bde-48ea-aff6-277b71365415" />
<br><br>

Si la prova anterior ha funcionat correctament, utilitzarem el codi de l'arxiu **login-and-post.html** per obtenir el token de l'usuari **editor1** i crear un post:

<img width="550" alt="login-and-post" src="https://github.com/user-attachments/assets/e912cd41-7ffa-4f6b-8b67-76f0b6233b16" />
<br><br>

**Resolució d'errors:** Aquestes proves poden presentar errors d'autenticació o creació de posts:
* Revisa que hi ha almenys un post o afegeix un de nou si l'arxiu **get-posts.html** no et mostra res.
* Si l'autenticació JWT no funciona, revisa que el codi dels arxius conté l'IP de la teva màquina virtual.
<br><br>

Si ambdues proves han resultat exitoses, tot indica que ja podem començar la migració del projecte anterior cap a **WordPress** mitjançant **API REST** i **Fetch API**.

<br><br>

## 4. Migració Automàtica

Gràcies a l'arxiu **migrador.html**, realitzarem les següents accions automàticament:
* Validarem l'usari per rebre el token.
* Netejarem l'HTML per a que no [...] * Crearem cada pàgina nova amb els arxius **.html**, **.css**, **.js** i **.png** / **.jpg** fusionats.

<img width="650" alt="validacio-migrador" src="https://github.com/user-attachments/assets/e55d925a-5b12-4c63-a894-d4a012714504" />
<br><br>
<img width="650" alt="migrador" src="https://github.com/user-attachments/assets/95121dff-14c8-4235-b1ad-3146d983a78b" />

<br>
<br>

## 5. Resultat Final
<img width="450" alt="pagina-inici" src="https://github.com/user-attachments/assets/541bf6e8-644c-444f-adf6-b3d216286644" />
