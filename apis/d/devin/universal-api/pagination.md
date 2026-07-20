# Devin Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Devin expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-knowledge-notes?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Devin actions that support pagination

- [List Knowledge Notes](actions/list-knowledge-notes.md)
- [List Playbooks](actions/list-playbooks.md)
- [List Secrets](actions/list-secrets.md)
- [List Sessions](actions/list-sessions.md)
- [List Sessions With Insights](actions/list-sessions-with-insights.md)
