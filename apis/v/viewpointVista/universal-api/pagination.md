# Viewpoint Vista Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Viewpoint Vista expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/list-ap-objects?connectionId=$CONNECTION_ID&limit=25&offset=0&object=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Viewpoint Vista actions that support pagination

- [List AP Objects](actions/list-ap-objects.md)
- [List AR Objects](actions/list-ar-objects.md)
- [List DM Objects](actions/list-dm-objects.md)
- [List EM Objects](actions/list-em-objects.md)
- [List GL Objects](actions/list-gl-objects.md)
- [List HQ Objects](actions/list-hq-objects.md)
- [List HR Objects](actions/list-hr-objects.md)
- [List IN Objects](actions/list-in-objects.md)
- [List JC Objects](actions/list-jc-objects.md)
- [List MS Objects](actions/list-ms-objects.md)
- [List PM Objects](actions/list-pm-objects.md)
- [List PO Objects](actions/list-po-objects.md)
- [List Potential Projects](actions/list-potential-projects.md)
- [List PR Objects](actions/list-pr-objects.md)
- [List SL Objects](actions/list-sl-objects.md)
- [List SM Objects](actions/list-sm-objects.md)
- [List UD Objects](actions/list-ud-objects.md)
- [Search AP Objects](actions/search-ap-objects.md)
- [Search AR Objects](actions/search-ar-objects.md)
- [Search Batch Entries](actions/search-batch-entries.md)
- [Search Batches](actions/search-batches.md)
- [Search DM Objects](actions/search-dm-objects.md)
- [Search EM Objects](actions/search-em-objects.md)
- [Search GL Objects](actions/search-gl-objects.md)
- [Search HQ Objects](actions/search-hq-objects.md)
- [Search HR Objects](actions/search-hr-objects.md)
- [Search IN Objects](actions/search-in-objects.md)
- [Search JC Objects](actions/search-jc-objects.md)
- [Search MS Objects](actions/search-ms-objects.md)
- [Search PM Objects](actions/search-pm-objects.md)
- [Search PO Objects](actions/search-po-objects.md)
- [Search Potential Projects](actions/search-potential-projects.md)
- [Search PR Objects](actions/search-pr-objects.md)
- [Search SL Objects](actions/search-sl-objects.md)
- [Search SM Objects](actions/search-sm-objects.md)
- [Search Transactions](actions/search-transactions.md)
- [Search UD Objects](actions/search-ud-objects.md)
