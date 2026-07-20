# Coda Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Coda expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-columns?connectionId=$CONNECTION_ID&limit=25&offset=0&docId=string&tableIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Coda actions that support pagination

- [List Columns](actions/list-columns.md)
- [List Controls](actions/list-controls.md)
- [List Docs](actions/list-docs.md)
- [List Formulas](actions/list-formulas.md)
- [List Pages](actions/list-pages.md)
- [List Rows](actions/list-rows.md)
- [List Tables](actions/list-tables.md)
