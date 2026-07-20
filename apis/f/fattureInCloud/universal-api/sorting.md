# Fatture in Cloud Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Fatture in Cloud expects, and each action page lists the fields available to sort.

## Fatture in Cloud actions that support sorting

- [List Clients](actions/list-clients.md)
- [List Issued Documents](actions/list-issued-documents.md)
- [List Products](actions/list-products.md)
- [List Receipts](actions/list-receipts.md)
- [List Received Documents](actions/list-received-documents.md)
- [List Suppliers](actions/list-suppliers.md)
