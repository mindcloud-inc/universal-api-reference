# Boost Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Boost expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Boost actions that support filtering

- [List Activities](actions/list-activities.md)
- [List Addresses](actions/list-addresses.md)
- [List AppFlows](actions/list-appflows.md)
- [List Automation Actions](actions/list-automation-actions.md)
- [List Automation Triggers](actions/list-automation-triggers.md)
- [List Business Cases](actions/list-business-cases.md)
- [List Business Contracts](actions/list-business-contracts.md)
- [List Business Offers](actions/list-business-offers.md)
- [List Business Orders](actions/list-business-orders.md)
- [List Charts](actions/list-charts.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Custom Modules](actions/list-custom-modules.md)
- [List Dashboards](actions/list-dashboards.md)
- [List Files](actions/list-files.md)
- [List Forms](actions/list-forms.md)
- [List Spaces](actions/list-spaces.md)
- [List Users](actions/list-users.md)
