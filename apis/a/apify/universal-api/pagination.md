# Apify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Apify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-dataset-items?connectionId=$CONNECTION_ID&limit=25&offset=0&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Apify actions that support pagination

- [Get Dataset Items](actions/get-dataset-items.md)
- [List Actor Tasks](actions/list-actor-tasks.md)
- [List Actors](actions/list-actors.md)
- [List Datasets](actions/list-datasets.md)
- [List Key-Value Stores](actions/list-key-value-stores.md)
- [List Request Queues](actions/list-request-queues.md)
