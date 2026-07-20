# OpenPLZ Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model OpenPLZ expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria?connectionId=$CONNECTION_ID&limit=25&offset=0&searchTerm=Wien%20Stephansplatz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## OpenPLZ actions that support pagination

- [Full Text Search Austria](actions/full-text-search-austria.md)
- [Full Text Search Germany](actions/full-text-search-germany.md)
- [Full Text Search Liechtenstein](actions/full-text-search-liechtenstein.md)
- [Full Text Search Switzerland](actions/full-text-search-switzerland.md)
- [List Austrian Districts by Federal Province](actions/list-austrian-districts-by-federal-province.md)
- [List Austrian Municipalities by Federal Province](actions/list-austrian-municipalities-by-federal-province.md)
- [List German Districts by Federal State](actions/list-german-districts-by-federal-state.md)
- [List German Government Regions by Federal State](actions/list-german-government-regions-by-federal-state.md)
- [List German Municipalities by Federal State](actions/list-german-municipalities-by-federal-state.md)
- [List Swiss Communes by Canton](actions/list-swiss-communes-by-canton.md)
- [List Swiss Districts by Canton](actions/list-swiss-districts-by-canton.md)
- [List Swiss Localities by Canton](actions/list-swiss-localities-by-canton.md)
- [Search Austrian Localities](actions/search-austrian-localities.md)
- [Search Austrian Streets](actions/search-austrian-streets.md)
- [Search German Localities](actions/search-german-localities.md)
- [Search German Streets](actions/search-german-streets.md)
- [Search Liechtenstein Localities](actions/search-liechtenstein-localities.md)
- [Search Liechtenstein Streets](actions/search-liechtenstein-streets.md)
- [Search Swiss Localities](actions/search-swiss-localities.md)
- [Search Swiss Streets](actions/search-swiss-streets.md)
