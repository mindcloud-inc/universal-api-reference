# Bluebarry Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Bluebarry expects, and each action page lists the fields available to sort.

## Bluebarry actions that support sorting

- [List Advisors](actions/list-advisors.md)
- [List Answers](actions/list-answers.md)
- [List Landing Pages](actions/list-landing-pages.md)
- [List Live Product Feeds](actions/list-live-product-feeds.md)
- [List Products](actions/list-products.md)
- [List Questions](actions/list-questions.md)
- [List Settings](actions/list-settings.md)
- [List Webhook Subscriptions](actions/list-webhook-subscriptions.md)
