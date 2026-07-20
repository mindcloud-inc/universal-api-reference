# Geral Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Geral expects, and each action page lists the fields available to sort.

## Geral actions that support sorting

- [List Account Logs](actions/list-account-logs.md)
- [List Collected Data](actions/list-collected-data.md)
- [List Domains](actions/list-domains.md)
- [List Links](actions/list-links.md)
- [List Notification Handlers](actions/list-notification-handlers.md)
- [List Payments](actions/list-payments.md)
- [List Pixels](actions/list-pixels.md)
- [List QR Codes](actions/list-qr-codes.md)
- [List Splash Pages](actions/list-splash-pages.md)
