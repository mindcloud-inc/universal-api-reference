# MojoTxt Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format MojoTxt expects, and each action page lists the fields available to sort.

## MojoTxt actions that support sorting

- [Export Donations](actions/export-donations.md)
- [List Donations](actions/list-donations.md)
- [List Message Log](actions/list-message-log.md)
- [List Messages](actions/list-messages.md)
- [List Phone Number Subscribers](actions/list-phone-number-subscribers.md)
- [List Phone Numbers](actions/list-phone-numbers.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Subscription Lists](actions/list-subscription-lists.md)
