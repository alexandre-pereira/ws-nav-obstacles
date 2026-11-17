# ws-nav-obstacles

Paquets d'obstacles aériens et de sites de vol libre de l'application **WS Nav** (WeSoar), pour le monde entier,
reconstruits chaque semaine par GitHub Actions ([`.github/workflows/packs.yml`](.github/workflows/packs.yml)).

- **Obstacles** : lignes électriques, téléphériques, télésièges, câbles, mâts et éoliennes d'OpenStreetMap
  (extraits Geofabrik), et, en Suisse, les obstacles officiels de l'OFAC.
- **Sites** : décollages et atterrissages (`free_flying:site`) d'OpenStreetMap.
- Découpés en carrés de 1° ; chaque semaine une *release* (`packs-*.zip` + `manifest.json`), que le serveur de
  l'application (nav.wesoar.fr) récupère et sert aux téléphones.

Le dépôt est public pour que la construction ne coûte rien (minutes GitHub Actions gratuites pour un dépôt public).
Si un jour il faut économiser des minutes : variable de dépôt `PACKS_ROTATE` = N, l'Europe est refaite chaque
semaine et chaque autre partie du monde une semaine sur N (les autres semaines, ses paquets de la release précédente).

## Données et licences

- Données OpenStreetMap © les contributeurs d'OpenStreetMap, sous licence
  [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/) ; les paquets (base de données dérivée) sont sous ODbL 1.0.
- Obstacles suisses : © OFAC (Office fédéral de l'aviation civile), jeu de données ouvert de data.geo.admin.ch.
- `tools/build.mjs` : © WeSoar, tous droits réservés (assemblé depuis le code de WS Nav).

Contact : alex@wesoar.fr
