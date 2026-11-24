<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Monitoraggio: che cosa si legge e con quale esito

[English](README.en.md)

Come global-law monitora ogni paese: [global-law monitoring/](https://github.com/lexifina/global-law/tree/main/monitoring). Questa pagina fa lo stesso per Toscana soltanto: ogni lettura di una fonte ufficiale, quando è avvenuta e con quale esito (atti aggiunti, modificati e rimossi). La forma leggibile dalle macchine è [data/checks/](../data/checks/) (JSON Lines, schema `lexifina-check/1`), in `git log` come commit `Kind: check`, e mese per mese in [checks/](checks/).

**Ultimo controllo:** 2026-11-24 01:01 UTC, Raccolta normativa (Consiglio regionale della Toscana): 145 indirizzi letti; 3 aggiunti, 0 modificati, 0 rimossi; modifiche trovate; 2 non pubblicati, di cui 0 senza motivo.

## Fonti

| Fonte | Cartelle | Frequenza | Ultimo controllo riuscito | Ultimo esito | Stato |
| --- | --- | --- | --- | --- | --- |
| [Raccolta normativa (Consiglio regionale della Toscana)](https://raccoltanormativa.consiglio.regione.toscana.it/) | `lr/`, `statuto/` | ogni giorno | 2026-11-24 01:01 UTC | modifiche trovate | sorvegliata: gli zip dei dati aperti si sono fermati a gennaio 2022 e la ricerca del sito richiede una sessione del browser, quindi le leggi nuove si trovano come le ha trovate il costruttore (citazioni e prove di data); un numero che nessuno dei due trova è contato nella nota del controllo |

## Gli ultimi 30 giorni

| Inizio (UTC) | Fonte | Letti | Aggiunti | Modificati | Rimossi | Non pubblicati (senza motivo) | Esito | Commit |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | ---: |
| [2026-11-24 00:53](checks/2026-11.md#it-raccolta-toscana-20261124t005315z) | raccolta-toscana | 145 | 3 | 0 | 0 | 2 (0) | modifiche trovate | [4](https://github.com/lexifina/italy-tuscany-law/compare/1e20ecebb0cb...a8d0defff5d0) |
| [2026-11-24 00:41](checks/2026-11.md#it-raccolta-toscana-20261124t004115z) | raccolta-toscana | 144 | 1 | 1 | 2 | 2 (0) | modifiche trovate `audit-disagrees` | [3](https://github.com/lexifina/italy-tuscany-law/compare/3638a7a72e6a...3aff05d95068) |

## Verificalo da te

```
python tools/checktrail.py                      # l'ultimo controllo di ogni fonte
python tools/checktrail.py --day 2026-11-23     # tutti i controlli di un giorno
python tools/checktrail.py --act <id>           # quando un atto è stato visto e pubblicato
git log --grep='^Kind: check' --format='%ci %s'  # i controlli nella cronologia
```

Ha valore legale solo la pubblicazione ufficiale; i testi qui sono copie per la lettura e la ricerca.
