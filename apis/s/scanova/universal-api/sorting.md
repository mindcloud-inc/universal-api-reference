# Scanova Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Scanova expects, and each action page lists the fields available to sort.

## Scanova actions that support sorting

- [Get QR Code List](actions/get-qr-code-list.md)
