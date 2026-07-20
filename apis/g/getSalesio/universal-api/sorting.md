# GetSales.io Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format GetSales.io expects, and each action page lists the fields available to sort.

## GetSales.io actions that support sorting

- [List Automations](actions/list-automations.md)
- [List Emails](actions/list-emails.md)
- [List LinkedIn Messages](actions/list-linked-in-messages.md)
- [List Lists](actions/list-lists.md)
- [List Sender Profiles](actions/list-sender-profiles.md)
