# openFDA Drug Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format openFDA Drug expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## openFDA Drug actions that support filtering

- [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md)
- [Count Drug Enforcement Records](actions/count-drug-enforcement-records.md)
- [Count Drug Label Records](actions/count-drug-label-records.md)
- [Count Drug NDC Records](actions/count-drug-ndc-records.md)
- [Count Drug Shortage Records](actions/count-drug-shortage-records.md)
- [Count Drugs@FDA Records](actions/count-drugs-fda-records.md)
- [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md)
- [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md)
- [Search Drug Label Records](actions/search-drug-label-records.md)
- [Search Drug NDC Records](actions/search-drug-ndc-records.md)
- [Search Drug Shortage Records](actions/search-drug-shortage-records.md)
- [Search Drugs@FDA Records](actions/search-drugs-fda-records.md)
