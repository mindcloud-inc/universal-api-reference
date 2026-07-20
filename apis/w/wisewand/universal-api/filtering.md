# Wisewand Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Wisewand expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Wisewand actions that support filtering

- [Get all authors](actions/get-all-authors.md)
- [Get all categories](actions/get-all-categories.md)
- [Get daily summary of transactions](actions/get-daily-summary-of-transactions.md)
- [Get entity counts summary](actions/get-entity-counts-summary.md)
- [Get the result of articles](actions/get-the-result-of-articles.md)
- [Get the result of categorypages](actions/get-the-result-of-categorypages.md)
- [Get the result of discoverarticles](actions/get-the-result-of-discoverarticles.md)
- [Get the result of productpages](actions/get-the-result-of-productpages.md)
- [Get the result of updateposts](actions/get-the-result-of-updateposts.md)
- [List articles](actions/list-articles.md)
- [List categorypages](actions/list-categorypages.md)
- [List connections](actions/list-connections.md)
- [List discoverarticles](actions/list-discoverarticles.md)
- [List feeds](actions/list-feeds.md)
- [List personas](actions/list-personas.md)
- [List productpages](actions/list-productpages.md)
- [List projects](actions/list-projects.md)
- [List transactions](actions/list-transactions.md)
- [List updateposts](actions/list-updateposts.md)
