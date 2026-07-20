# TelTel Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format TelTel expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## TelTel actions that support filtering

- [List Available Number Countries](actions/list-available-number-countries.md)
- [List Available Number Price Groups](actions/list-available-number-price-groups.md)
- [List Calls](actions/list-calls.md)
- [List Contact Group Contacts](actions/list-contact-group-contacts.md)
- [List Contact Groups](actions/list-contact-groups.md)
- [List Contacts](actions/list-contacts.md)
- [List Inbound SMS Reports](actions/list-inbound-sms-reports.md)
- [List Number Orders](actions/list-number-orders.md)
- [List Phone Numbers](actions/list-phone-numbers.md)
- [List SMS Campaigns](actions/list-sms-campaigns.md)
- [List SMS Reports](actions/list-sms-reports.md)
