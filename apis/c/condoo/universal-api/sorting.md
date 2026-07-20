# condoo Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format condoo expects, and each action page lists the fields available to sort.

## condoo actions that support sorting

- [List Account Logs](actions/list-account-logs.md)
- [List Account Payments](actions/list-account-payments.md)
- [List Custom Domains](actions/list-custom-domains.md)
- [List Goal Conversions](actions/list-goal-conversions.md)
- [List Goals](actions/list-goals.md)
- [List Pageviews](actions/list-pageviews.md)
- [List Websites](actions/list-websites.md)
