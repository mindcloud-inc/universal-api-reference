# ActiveCampaign Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format ActiveCampaign expects, and each action page lists the fields available to sort.

## ActiveCampaign actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Deal Stages](actions/list-deal-stages.md)
- [List Deals](actions/list-deals.md)
- [List Lists](actions/list-lists.md)
- [List Pipelines](actions/list-pipelines.md)
