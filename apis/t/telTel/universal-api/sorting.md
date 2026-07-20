# TelTel Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format TelTel expects, and each action page lists the fields available to sort.

## TelTel actions that support sorting

- [List Calls](actions/list-calls.md)
- [List Contact Group Contacts](actions/list-contact-group-contacts.md)
- [List Contact Groups](actions/list-contact-groups.md)
- [List Contacts](actions/list-contacts.md)
- [List Inbound SMS Reports](actions/list-inbound-sms-reports.md)
- [List SMS Campaigns](actions/list-sms-campaigns.md)
- [List SMS Reports](actions/list-sms-reports.md)
