<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Monitoring: what is read and what came of it

[Italiano](README.md)

How global-law monitors every country: [global-law monitoring/](https://github.com/lexifina/global-law/tree/main/monitoring). This page is the same for Tuscany only: every time an official source is read, when, and what came of it (acts added, changed and removed). The machine-readable form is [data/checks/](../data/checks/) (JSON Lines, schema `lexifina-check/1`), in `git log` as `Kind: check` commits, and month by month in [checks/](checks/).

**Last check:** 2026-11-24 01:01 UTC, Raccolta normativa (Consiglio regionale della Toscana): 145 addresses read; 3 added, 0 changed, 0 removed; changes found; 2 not published, 0 of them with no reason.

## Sources

| Source | Folders | How often | Last successful check | Last result | State |
| --- | --- | --- | --- | --- | --- |
| [Raccolta normativa (Consiglio regionale della Toscana)](https://raccoltanormativa.consiglio.regione.toscana.it/) | `lr/`, `statuto/` | daily | 2026-11-24 01:01 UTC | changes found | watched: the open-data zips stopped in January 2022 and the site's search needs a browser session, so new laws are found as the builder found them (citations and date probes); a number neither finds is counted in the check's note |

## The last 30 days

| Started (UTC) | Source | Read | Added | Changed | Removed | Not published (no reason) | Result | Commits |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | ---: |
| [2026-11-24 00:53](checks/2026-11.md#it-raccolta-toscana-20261124t005315z) | raccolta-toscana | 145 | 3 | 0 | 0 | 2 (0) | changes found | [4](https://github.com/lexifina/italy-tuscany-law/compare/1e20ecebb0cb...a8d0defff5d0) |
| [2026-11-24 00:41](checks/2026-11.md#it-raccolta-toscana-20261124t004115z) | raccolta-toscana | 144 | 1 | 1 | 2 | 2 (0) | changes found `audit-disagrees` | [3](https://github.com/lexifina/italy-tuscany-law/compare/3638a7a72e6a...3aff05d95068) |

## Check it yourself

```
python tools/checktrail.py                      # the latest check of every source
python tools/checktrail.py --day 2026-11-23     # every check of a day
python tools/checktrail.py --act <id>           # when an act was seen and published
git log --grep='^Kind: check' --format='%ci %s'  # the checks in the history
```

Only the official publication has legal force; the texts here are copies for reading and searching.
