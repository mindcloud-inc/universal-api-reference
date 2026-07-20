# Conveyor Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Conveyor expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Conveyor actions that support pagination

- [List Connections](actions/list-connections.md)
- [List Interactions](actions/list-interactions.md)
- [List Interactions By Connection](actions/list-interactions-by-connection.md)
- [List Interactions By Document](actions/list-interactions-by-document.md)
- [List Interactions By Question](actions/list-interactions-by-question.md)
- [List Knowledge Base Questions](actions/list-knowledge-base-questions.md)
