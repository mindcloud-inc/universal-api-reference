# Adafruit IO Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Adafruit IO expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/list-actions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Adafruit IO actions that support pagination

- [List Actions](actions/list-actions.md)
- [List Feed Data](actions/list-feed-data.md)
- [List Feeds](actions/list-feeds.md)
- [List Group Feeds](actions/list-group-feeds.md)
- [List Groups](actions/list-groups.md)
- [List Tokens](actions/list-tokens.md)
