# Letta Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Letta expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-agent-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Letta actions that support pagination

- [List Agent Messages](actions/list-agent-messages.md)
- [List Agents](actions/list-agents.md)
- [List Blocks](actions/list-blocks.md)
- [List Conversations](actions/list-conversations.md)
- [List Models](actions/list-models.md)
- [List Runs](actions/list-runs.md)
- [List Tools](actions/list-tools.md)
