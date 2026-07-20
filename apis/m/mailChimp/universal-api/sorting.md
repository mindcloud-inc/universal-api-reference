# Mailchimp Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Mailchimp expects, and each action page lists the fields available to sort.

## Mailchimp actions that support sorting

- [List Audience Members](actions/list-audience-members.md)
- [List Audiences](actions/list-audiences.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Templates](actions/list-templates.md)
