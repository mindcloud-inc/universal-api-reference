# Congress.gov Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Congress.gov expects, and each action page lists the fields available to sort.

## Congress.gov actions that support sorting

- [List Bill Cosponsors](actions/list-bill-cosponsors.md)
- [List Summaries](actions/list-summaries.md)
- [List Summaries By Congress](actions/list-summaries-by-congress.md)
- [List Summaries By Congress And Bill Type](actions/list-summaries-by-congress-and-bill-type.md)
