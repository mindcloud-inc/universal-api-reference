# Centerpoint Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Centerpoint expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Centerpoint actions that support filtering

- [List Budget Entries](actions/list-budget-entries.md)
- [List Budget Types](actions/list-budget-types.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Cost Codes](actions/list-cost-codes.md)
- [List Employees](actions/list-employees.md)
- [List Invoices](actions/list-invoices.md)
- [List Locations](actions/list-locations.md)
- [List Materials](actions/list-materials.md)
- [List Model Files](actions/list-model-files.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Product Template Tags](actions/list-product-template-tags.md)
- [List Product Templates](actions/list-product-templates.md)
- [List Production Days](actions/list-production-days.md)
- [List Production Items](actions/list-production-items.md)
- [List Production Materials](actions/list-production-materials.md)
- [List Productions](actions/list-productions.md)
- [List Products](actions/list-products.md)
- [List Properties](actions/list-properties.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Service Agreements](actions/list-service-agreements.md)
- [List Services](actions/list-services.md)
- [List Tasks](actions/list-tasks.md)
- [List Tax Codes](actions/list-tax-codes.md)
- [List Warranties](actions/list-warranties.md)
- [List Work Time Entries](actions/list-work-time-entries.md)
