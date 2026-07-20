# Webex Interact Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Webex Interact expects, and each action page lists the fields available to sort.

## Webex Interact actions that support sorting

- [Filter shortlinks](actions/filter-shortlinks.md)
- [List contact lists](actions/list-contact-lists.md)
- [List scheduled SMS by created date range](actions/list-scheduled-sms-by-created-date-range.md)
- [List scheduled SMS by scheduled date range](actions/list-scheduled-sms-by-scheduled-date-range.md)
