# Instatus Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Instatus expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-components?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Instatus actions that support pagination

- [List Components](actions/list-components.md)
- [List Incidents](actions/list-incidents.md)
- [List Maintenances](actions/list-maintenances.md)
- [List Status Pages](actions/list-status-pages.md)
- [List Subscribers](actions/list-subscribers.md)
