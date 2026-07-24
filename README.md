# nol.log

Journalisation à niveaux en pur [Nolc](https://github.com/Noliae-France/nolc), sans dépendance.

## Installation

```toml
[dependances]
"nol-log" = { git = "https://github.com/Noliae-France/nol-log" }
```

## API
Quatre niveaux (0=debug, 1=info, 2=warn, 3=error). Un journal filtre selon son seuil ; chaque ligne porte un horodatage epoch.

```nol
let j = journal_neuf(1)          // seuil INFO
log_debug(j, "ignoré")           // sous le seuil
log_info(j, "démarrage")         // [INFO] 1690000000 démarrage
log_erreur(j, "panne")           // [ERROR] 1690000000 panne
```

## Licence

MIT © 2026 Bastien LANGUEDOC.
