# Notifyre SMS Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Notifyre SMS expects, and each action page lists the fields available to sort.

## Notifyre SMS actions that support sorting

- [List Groups](actions/list-groups.md)
- [List Received Faxes](actions/list-received-faxes.md)
- [List Sent Faxes](actions/list-sent-faxes.md)
- [List SMS Replies](actions/list-sms-replies.md)
