# Zenvoices Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Zenvoices expects, and each action page lists the fields available to sort.

## Zenvoices actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Administrations](actions/list-administrations.md)
- [List Cost Centres](actions/list-cost-centres.md)
- [List Cost Units](actions/list-cost-units.md)
- [List Employees](actions/list-employees.md)
- [List Financial Transactions](actions/list-financial-transactions.md)
- [List Inbox Documents](actions/list-inbox-documents.md)
- [List Ledger Accounts](actions/list-ledger-accounts.md)
- [List Payment Conditions](actions/list-payment-conditions.md)
- [List Products](actions/list-products.md)
- [List Projects](actions/list-projects.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Tax Codes](actions/list-tax-codes.md)
