# Influenza and Covid-19 Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Influenza and Covid-19 expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Influenza and Covid-19 actions that support filtering

- [List Emergency Department Respiratory Daily](actions/list-emergency-department-respiratory-daily.md)
- [List Emergency Department Visits by Demographic Category](actions/list-emergency-department-visits-by-demographic-category.md)
- [List Provisional Respiratory Death Percentages](actions/list-provisional-respiratory-death-percentages.md)
- [List Viral Respiratory Test Positivity](actions/list-viral-respiratory-test-positivity.md)
