# RD Station CRM Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format RD Station CRM expects, and each action page lists the fields available to sort.

## RD Station CRM actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Organizations](actions/list-organizations.md)
- [List Pipeline Stages](actions/list-pipeline-stages.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Sources](actions/list-sources.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)
