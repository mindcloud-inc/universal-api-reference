# Avalara AvaTax Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Avalara AvaTax expects, and each action page lists the fields available to sort.

## Avalara AvaTax actions that support sorting

- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Entity Use Codes](actions/list-entity-use-codes.md)
- [List Items By Company](actions/list-items-by-company.md)
- [List Jurisdictions Hierarchy](actions/list-jurisdictions-hierarchy.md)
- [List Nexus By Company](actions/list-nexus-by-company.md)
- [List Parameters](actions/list-parameters.md)
- [List Tax Authority Types](actions/list-tax-authority-types.md)
- [List Tax Codes By Company](actions/list-tax-codes-by-company.md)
- [List Tax Rules](actions/list-tax-rules.md)
- [List Transactions By Company](actions/list-transactions-by-company.md)
- [Query Companies](actions/query-companies.md)
- [Query Customers](actions/query-customers.md)
- [Query Tax Codes](actions/query-tax-codes.md)
