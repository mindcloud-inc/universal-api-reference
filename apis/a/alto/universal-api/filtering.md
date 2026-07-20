# Alto Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Alto expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Alto actions that support filtering

- [Filter Inventory](actions/filter-inventory.md)
- [Filter Listings](actions/filter-listings.md)
- [Get All Contacts](actions/get-all-contacts.md)
- [Get Branches](actions/get-branches.md)
- [Get Contact Relationships](actions/get-contact-relationships.md)
- [Get Contacts](actions/get-contacts.md)
- [Get Documents](actions/get-documents.md)
- [Get Inventory](actions/get-inventory.md)
- [Get Inventory Documents](actions/get-inventory-documents.md)
- [Get Inventory Items](actions/get-inventory-items.md)
- [Get Landlords](actions/get-landlords.md)
- [Get Leads](actions/get-leads.md)
- [Get Negotiator Appointments](actions/get-negotiator-appointments.md)
- [Get Owners](actions/get-owners.md)
- [Get Property Listings](actions/get-property-listings.md)
- [Get Tenancies](actions/get-tenancies.md)
- [Get Valuations](actions/get-valuations.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Inventory](actions/search-inventory.md)
