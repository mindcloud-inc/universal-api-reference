# WebinarGeek Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format WebinarGeek expects, and each action page lists the fields available to sort.

## WebinarGeek actions that support sorting

- [List Broadcasts](actions/list-broadcasts.md)
- [List Messages](actions/list-messages.md)
- [List Questions](actions/list-questions.md)
- [List Subscription Payments](actions/list-subscription-payments.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Webinars](actions/list-webinars.md)
