# ChargeLocator data

Public distribution of the offline data packs used by the ChargeLocator Android app: one pack per country,
built daily by an automated job from official open charging data. No code, only releases.

- Manifest (list of packs of the latest release): [`datapacks-v1.json`](../../releases/latest/download/datapacks-v1.json)
- Packs: `datapack-v1-<country>.json.gz`, e.g. [`datapack-v1-nl.json.gz`](../../releases/latest/download/datapack-v1-nl.json.gz);
  Germany also as [`datapack-v1.json.gz`](../../releases/latest/download/datapack-v1.json.gz) (older app versions)
- Format v1: gzip-compressed JSON `{"v":1,"generatedAt":…,"country":"NL","source":"NDW","idPrefix":"ndw","currency":"EUR","stations":[…]}`
  with compact keys (`i` id, `n` name, `o` operator, `a`/`g` lat/lng, `k` connectors `type|current|kW|count`,
  `$` ad-hoc price `[per kWh, per minute, session fee, blocking fee/min, blocking after min, updated]`).

## Sources, licences and attribution

| Country | Source | Licence |
|---|---|---|
| Germany | Charge point operators via the National Access Point [Mobilithek](https://mobilithek.info) (EU regulation AFIR) | Licence terms of the individual Mobilithek offers |
| Netherlands | [NDW – Nationaal Dataportaal Wegverkeer](https://opendata.ndw.nu) (DOT-NL) | CC0 1.0 |
| France | [transport.data.gouv.fr – Base nationale consolidée des IRVE](https://transport.data.gouv.fr) | Licence Ouverte / Open Licence 2.0 (Etalab); the date of the last update is in each release and pack (`generatedAt`) |
| Switzerland | Swiss Federal Office of Energy SFOE – [ich-tanke-strom.ch](https://ich-tanke-strom.ch), dataset "Charging stations for electric cars" ([opendata.swiss](https://opendata.swiss/dataset/ladestationen-fuer-elektroautos)) | SFOE terms: open use, source required; data ownership remains with the charge point operators |

Data has been summarised (charge points grouped into locations, prices simplified and converted to consumer prices).
Prices are ad-hoc prices as published by the operators; the price shown at the charger is binding. No guarantee of
completeness or correctness.

## Privacy policy

The Charge Locator privacy policy is maintained at https://astronlabs.dev/privacy/chargelocator.html.
`privacy.html` in this repo only redirects there (kept so old app versions and links keep working).
