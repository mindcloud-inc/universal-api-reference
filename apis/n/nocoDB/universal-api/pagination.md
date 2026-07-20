# NocoDB Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model NocoDB expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-linked-records?connectionId=$CONNECTION_ID&limit=25&offset=0&baseId=string&tableId=string&linkFieldId=https%3A%2F%2Fexample.com&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## NocoDB actions that support pagination

- [List Linked Records](actions/list-linked-records.md)
- [List Table Records](actions/list-table-records.md)
