# ChargeLocator data

Public distribution of the offline data pack used by the ChargeLocator Android app. No code, only
releases. Built daily by an automated job from the official AFIR data of German charge point operators.

- Latest pack: [`datapack-v1.json.gz`](../../releases/latest/download/datapack-v1.json.gz)
- Format v1: gzip-compressed JSON `{"v":1,"generatedAt":…,"stations":[…]}` with compact keys
  (`i` id, `n` name, `o` operator, `a`/`g` lat/lng, `k` connectors `type|current|kW|count`,
  `$` ad-hoc price `[per kWh, per minute, session fee, blocking fee/min, blocking after min, updated]`).

## Source and attribution

Data: charge point operators, published under the EU regulation AFIR via the German National Access
Point [Mobilithek](https://mobilithek.info). The licence terms of the individual data offers apply
(see the offers on the Mobilithek). Prices are ad-hoc prices as published by the operators; the price
shown at the charger is binding. No guarantee of completeness or correctness.
