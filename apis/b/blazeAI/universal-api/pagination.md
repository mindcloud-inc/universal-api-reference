# Blaze AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Blaze AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-brand-voices?connectionId=$CONNECTION_ID&limit=25&offset=0&workspace_id=994619" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Blaze AI actions that support pagination

- [List Brand Voices](actions/list-brand-voices.md)
- [List Doc Accesses](actions/list-doc-accesses.md)
- [List Doc Properties](actions/list-doc-properties.md)
- [List Docs](actions/list-docs.md)
- [List Folders](actions/list-folders.md)
- [List Group Users](actions/list-group-users.md)
- [List Groups](actions/list-groups.md)
- [List Handbook Items](actions/list-handbook-items.md)
- [List Handbooks](actions/list-handbooks.md)
- [List Users](actions/list-users.md)
- [List Workspace Properties](actions/list-workspace-properties.md)
