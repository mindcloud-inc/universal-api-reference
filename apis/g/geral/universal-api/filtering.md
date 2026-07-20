# Geral Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Geral expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Geral actions that support filtering

- [Get Link Statistics](actions/get-link-statistics.md)
- [List Account Logs](actions/list-account-logs.md)
- [List Collected Data](actions/list-collected-data.md)
- [List Domains](actions/list-domains.md)
- [List Links](actions/list-links.md)
- [List Notification Handlers](actions/list-notification-handlers.md)
- [List Payments](actions/list-payments.md)
- [List Pixels](actions/list-pixels.md)
- [List QR Codes](actions/list-qr-codes.md)
- [List Splash Pages](actions/list-splash-pages.md)
- [List Statistics](actions/list-statistics.md)
