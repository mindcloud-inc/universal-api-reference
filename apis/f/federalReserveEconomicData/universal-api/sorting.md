# Federal Reserve Economic Data Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Federal Reserve Economic Data expects, and each action page lists the fields available to sort.

## Federal Reserve Economic Data actions that support sorting

- [List Category Series](actions/list-category-series.md)
- [List Category Tags](actions/list-category-tags.md)
- [List Release Dates](actions/list-release-dates.md)
- [List Release Dates For Release](actions/list-release-dates-for-release.md)
- [List Release Series](actions/list-release-series.md)
- [List Releases](actions/list-releases.md)
- [List Series Observations](actions/list-series-observations.md)
- [List Source Releases](actions/list-source-releases.md)
- [List Sources](actions/list-sources.md)
- [Search Series](actions/search-series.md)
