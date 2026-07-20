# Bulldog-WP Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Bulldog-WP expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Bulldog-WP actions that support filtering

- [Get analytics](actions/get-analytics.md)
- [List campaign contacts](actions/get-campaign-contacts.md)
- [Get campaigns](actions/get-campaigns.md)
- [Search chat messages](actions/get-chat-messages.md)
- [Search chats](actions/get-device-chats.md)
- [List contacts](actions/get-device-contacts.md)
- [Search inbound files](actions/get-device-files.md)
- [Get numbers](actions/get-devices.md)
- [List labels](actions/get-labels.md)
- [Get users](actions/get-team-users.md)
- [List templates](actions/get-templates.md)
- [Get messaging prices](actions/get-waba-prices.md)
- [Get webhooks](actions/get-webhooks.md)
- [Search files](actions/search-files.md)
- [Search messages](actions/search-messages.md)
