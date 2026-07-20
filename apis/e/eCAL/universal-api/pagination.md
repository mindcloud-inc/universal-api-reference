# ECAL Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ECAL expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-batch-private-events-by-reference-type?connectionId=$CONNECTION_ID&limit=25&offset=0&referenceType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ECAL actions that support pagination

- [List Batch Private Events By Reference Type](actions/list-batch-private-events-by-reference-type.md)
- [List Batch Private Events By Subscriber](actions/list-batch-private-events-by-subscriber.md)
- [List Batch Private Events By Subscriber And Reference Type](actions/list-batch-private-events-by-subscriber-and-reference-type.md)
- [List Events](actions/list-events.md)
- [List Private Events](actions/list-private-events.md)
- [Search Batch Private Events By IDs](actions/search-batch-private-events-by-ids.md)
