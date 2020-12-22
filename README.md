# Valtimo Platform

### Wat is dit? 
- Serie Docker containers waarmee een compleet platform wordt geinstalleerd voor testdoeleinden. Inclusief OpenZaak.

### Hoe start ik Valtimo?
- Installeer Docker Desktop (inclusief Docker Compose): https://docs.docker.com/compose/install/
- Download deze repository
- Voer het volgende commando uit in een terminal:
```docker-compose up -d```

### Links
- Valtimo Console: http://localhost/
- KeyCloak: http://localhost:8081/
- Open Zaak: http://localhost:8000

### Services:
- Valtimo Server
- Valtimo Console
- MySQL database
- NGINX reverse proxy
- KeyCloak
- Open Zaak
  - Open Zaak
  - Redis 
  - Postgis

### Tips:
- Keycloak, Valtimo Console (de UI) en Valtimo Server zijn gekoppeld. Voor OpenZaak moet je zelf een user aanmaken, applicatie registreren en daarna de koppeling leggen in de Valtimo Console. Het voorbeeldproces werkt alleen als je OpenZaak koppelt. Als alternatief kun je zelf een proces en formulieren toevoegen en koppelen aan het Dossier "Bezwaren". We zullen een uitlegvideo maken hoe dit te doen.   

## Licentie
The source files in this repo are licensed to you under the EUPL 1.2. You can download the license in 23 languages: https://joinup.ec.europa.eu/collection/eupl/eupl-text-eupl-12. If you have any questions about the use of this codebase in a larger work: just ask us. 
All third party components are delivered under their own, original license.

### Hulp:
- je vindt een installatievideo op https://www.valtimo.nl/kennis/docker-installatie/
- tips op https://docs.valtimo.nl/
