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
  
### Additionele configuratie
#### Valtimo Server
De volgende environment variabelen kunnen worden opgegeven in de Valtimo Server container:
  - DATABASE_HOST (default: valtimo_database)
  - DATABASE_PORT (default: 3306)
  - DATABASE_NAME (default: valtimo)
  - DATABASE_USER (default: root)
  - DATABASE_PASSWORD (default: demo)

#### Valtimo Console
De configuratie van de Valtimo Console kan worden aangepast door middel van een config.json bestand. Deze moet dan als mount worden opgegeven in de docker-compose.yml:
```
volumes:
  - ./config.json:/config.json  
```

Onderstaande configuratie kan, per property, worden overschreven:
```
{
  "baseUrl": "http://localhost",
  "keycloak": {
    "url": "http://localhost:8081/auth",
    "realm": "valtimo",
    "clientId": "valtimo-console"
  },
  "openzaak": {
    "catalogusId": ""
  }
}
```

### Open Zaak
- Om in te kunnen loggen op de beheer-omgeving van Open Zaak voer je eerst een configuratiescript uit. Dit doe je door het volgende commando uit te voeren in een terminal:
```docker exec -u openzaak valtimo_openzaak_postgis psql postgres -f /tmp/openzaak-config.sql```

## Licentie
The source files in this repo are licensed to you under the EUPL 1.2. You can download the license in 23 languages: https://joinup.ec.europa.eu/collection/eupl/eupl-text-eupl-12. If you have any questions about the use of this codebase in a larger work: just ask us. 
All third party components are delivered under their own, original license.

### Hulp:
- je vindt een installatievideo op https://www.valtimo.nl/kennis/docker-installatie/
- tips op https://docs.valtimo.nl/
- https://forum.valtimo.nl/
