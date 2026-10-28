# Crypto prop firm rule changes

Every rule, price and payout change that [PropRubric](https://proprubric.com/) has verified at crypto prop firms, with the date, the old value, the new value and the firm's own source page.

PropRubric is an independent crypto prop firm research site run by the PropRubric Research Team. It reads each firm's own rules, prices and payout terms, records the date of every check, and logs every change, so crypto traders worldwide can see what a challenge really costs and what it takes to get paid, before they pay for it.

- Live log: https://proprubric.com/changes/
- Always-current CSV: https://proprubric.com/data/changes.csv
- RSS feed: https://proprubric.com/changes/feed.xml
- How values are verified: https://proprubric.com/methodology/

## File

`rule-changes.csv`, one row per verified change, newest first.

| Column | Meaning |
|---|---|
| `date` | Day the change was verified (YYYY-MM-DD) |
| `firm_id` | Firm slug, matching `https://proprubric.com/crypto/reviews/<firm_id>/` |
| `field` | The rule or value that changed |
| `old_value` | Value before the change |
| `new_value` | Value after the change |
| `source_url` | The firm's own page the new value was read from |
| `note` | What happened and when |
| `type` | `Firm change` (the firm changed its rule, 91 rows), `PropRubric correction` (PropRubric fixed its own record, 75) or `PropRubric addition` (a value recorded for the first time, 141) |

This copy is refreshed automatically every 6 hours from the live CSV by the GitHub Action in `.github/workflows/mirror-changes-csv.yml`, and a commit is made only when a row changed. The row counts above are kept in step by the same Action.

## License

Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Credit "PropRubric" with a link to https://proprubric.com/changes/.

Nothing here is financial advice. Prop firm challenges are paid evaluations on simulated accounts.
