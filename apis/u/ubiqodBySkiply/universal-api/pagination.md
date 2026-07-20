# Ubiqod by Skiply Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Ubiqod by Skiply expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-badge-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Ubiqod by Skiply actions that support pagination

- [List Badge Lists](actions/list-badge-lists.md)
- [List PIN Code Lists](actions/list-pin-code-lists.md)
- [List Sites](actions/list-sites.md)
- [List Trackers](actions/list-trackers.md)
