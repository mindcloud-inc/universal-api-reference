# Print.one Postcards Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Print.one Postcards expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-batch-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Print.one Postcards actions that support pagination

- [List Batch Orders](actions/list-batch-orders.md)
- [List Batches](actions/list-batches.md)
- [List Custom Files](actions/list-custom-files.md)
- [List Orders](actions/list-orders.md)
- [List Templates](actions/list-templates.md)
