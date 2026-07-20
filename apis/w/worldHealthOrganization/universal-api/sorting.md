# World Health Organization Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format World Health Organization expects, and each action page lists the fields available to sort.

## World Health Organization actions that support sorting

- [List Age Groups](actions/list-age-groups.md)
- [List Countries](actions/list-countries.md)
- [List Dimension Values](actions/list-dimension-values.md)
- [List Dimensions](actions/list-dimensions.md)
- [List Income Groups](actions/list-income-groups.md)
- [List Indicator Data](actions/list-indicator-data.md)
- [List Indicator Dimensions](actions/list-indicator-dimensions.md)
- [List Indicators](actions/list-indicators.md)
- [List Publish States](actions/list-publish-states.md)
- [List Region Countries](actions/list-region-countries.md)
- [List Sex Values](actions/list-sex-values.md)
- [List WHO Regions](actions/list-who-regions.md)
- [List Year Values](actions/list-year-values.md)
