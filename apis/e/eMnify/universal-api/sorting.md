# EMnify Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format EMnify expects, and each action page lists the fields available to sort.

## EMnify actions that support sorting

- [List Application Tokens](actions/list-application-tokens.md)
- [List Endpoint Events](actions/list-endpoint-events.md)
- [List Endpoints](actions/list-endpoints.md)
- [List Events](actions/list-events.md)
- [List SIMs](actions/list-sims.md)
