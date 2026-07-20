# Retell AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Retell AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-chat?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Retell AI actions that support pagination

- [List Chat](actions/list-chat.md)
- [List Chat Agents](actions/list-chat-agents.md)
- [List Phone Numbers](actions/list-phone-numbers.md)
- [List Retell LLMs](actions/list-retell-llms.md)
- [List Voice Agents](actions/list-voice-agents.md)
