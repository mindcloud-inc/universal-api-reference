# Hume Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Hume expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-chat-events?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Hume actions that support pagination

- [List chat events](actions/list-chat-events.md)
- [List chat group events](actions/list-chat-group-events.md)
- [List chat groups](actions/list-chat-groups.md)
- [List chats](actions/list-chats.md)
- [List config versions](actions/list-config-versions.md)
- [List configs](actions/list-configs.md)
- [List prompt versions](actions/list-prompt-versions.md)
- [List prompts](actions/list-prompts.md)
- [List tool versions](actions/list-tool-versions.md)
- [List tools](actions/list-tools.md)
- [List voices](actions/list-voices.md)
