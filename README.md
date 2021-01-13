# Valtimo Platform

### Wat is dit? 
- Serie Docker containers waarmee een compleet platform wordt geinstalleerd voor testdoeleinden. Inclusief OpenZaak.

### Hoe start ik Valtimo?
- Installeer Docker Desktop (inclusief Docker Compose): https://docs.docker.com/compose/install/
- Download deze repository
- Voer het volgende commando uit in een terminal:
```docker-compose up -d```
- Username + Password van Keycloak is demo / demo
- Username + Password van Valtimo is demo / demo
- OpenZaak: zie onder. 

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
  
### Open Zaak
- Om in te kunnen loggen op de beheer-omgeving van Open Zaak voer je eerst een configuratiescript uit. Dit doe je door het volgende commando uit te voeren in een terminal:
```docker exec -u openzaak valtimo-platform_valtimo_openzaak_postgis_1 psql postgres -f /tmp/openzaak-config.sql```

## Licentie
The source files in this repo are licensed to you under the EUPL 1.2. You can download the license in 23 languages: https://joinup.ec.europa.eu/collection/eupl/eupl-text-eupl-12. If you have any questions about the use of this codebase in a larger work: just ask us. 
All third party components are delivered under their own, original license.

### Hulp:
- je vindt een installatievideo op https://www.valtimo.nl/kennis/docker-installatie/
- tips op https://docs.valtimo.nl/
- https://forum.valtimo.nl/
