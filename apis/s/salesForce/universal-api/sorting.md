# Salesforce Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Salesforce expects, and each action page lists the fields available to sort.

## Salesforce actions that support sorting

- [List Billing Credit Notes](actions/list-billing-credit-notes.md)
- [List Billing Invoices](actions/list-billing-invoices.md)
- [List Credit Memos](actions/list-credit-memos.md)
- [List Invoices](actions/list-invoices.md)
- [List Orders](actions/list-orders.md)
- [List Quote Line Items](actions/list-quote-line-items.md)
- [List Quotes](actions/list-quotes.md)
