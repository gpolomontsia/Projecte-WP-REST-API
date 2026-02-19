# Projecte SPRINT2 - Migració a WordPress

Aquesta és una guia pràctica per realitzar el procés de migració del projecte SPRINT1 (fet amb codi vanilla) a un WordPress dockeritzat dins d'un Ubuntu Server mitjançant JavaScript i WP REST API.

## Requisits Previs

Per tal de realitzar aquesta practica correctament, s'han de tenir com a mínim els següents requisits previs:
* Màquina virtual Ubuntu Server (24.04 LTS preferiblement) accessible des de la xarxa (en aquest cas, des de 192.168.32.129).
* Servei **Docker.io** (paquet lleuger de docker) instal·lat amb **docker-compose**.
* Ganes d'aprendre i calentar-se el cap programant JS sense utilitzar Gemini Pro.

## 1. Desplegament amb Docker

Crearem una carpeta anomenada **projecte_wordpress** i dins d'aquesta l'arxiu **docker-compose.yml**, on afegirem els contenidors per a **WordPress** i **MariaDB** amb els seus respectius volums:

<img width="313" height="523" alt="docker-compose" src="https://github.com/user-attachments/assets/17ba7307-f132-49b1-a239-618d85008f94" />

Després d'executar **docker-compose up -d**, ja podrem accedir a **WordPress** des del navegador web inserint **192.168.32.169:8080**.

## 2. Configuració de WordPress
<img width="825" height="320" alt="plugin-jwt" src="https://github.com/user-attachments/assets/d9584439-104d-4a85-b8c5-c77d3e1e011f" />
<img width="826" height="321" alt="plugin-file-manager" src="https://github.com/user-attachments/assets/b0166d70-5f56-4204-b153-f4a36b349cb6" />
<img width="782" height="500" alt="Configuracio-JWT" src="https://github.com/user-attachments/assets/95f902d6-1047-4472-8108-c8a05ed9423a" />
<img width="878" height="331" alt="explorador-arxius" src="https://github.com/user-attachments/assets/21f87bd5-75a7-4ea6-b002-48dbb6dfc767" />
<img width="808" height="555" alt="edicio-wp-config" src="https://github.com/user-attachments/assets/e446de06-f068-4b3a-887d-ca869613cc4d" />

## 3. Connexió amb Fetch API
<img width="751" height="535" alt="get-posts" src="https://github.com/user-attachments/assets/d18cf527-2bde-48ea-aff6-277b71365415" />

## 4. El Migració Automàtica

## 5. Resultat Final
<img width="1031" height="863" alt="pagina-inici" src="https://github.com/user-attachments/assets/541bf6e8-644c-444f-adf6-b3d216286644" />
