# Bluebarry Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Bluebarry expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Bluebarry actions that support filtering

- [List Advisors](actions/list-advisors.md)
- [List Answers](actions/list-answers.md)
- [List Landing Pages](actions/list-landing-pages.md)
- [List Live Product Feeds](actions/list-live-product-feeds.md)
- [List Products](actions/list-products.md)
- [List Questions](actions/list-questions.md)
- [List Settings](actions/list-settings.md)
- [List Webhook Subscriptions](actions/list-webhook-subscriptions.md)
