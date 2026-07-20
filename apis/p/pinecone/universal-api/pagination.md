# Pinecone Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pinecone expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-imports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pinecone actions that support pagination

- [List Imports](actions/list-imports.md)
- [List Index Backups](actions/list-index-backups.md)
- [List Namespaces](actions/list-namespaces.md)
- [List Project Backups](actions/list-project-backups.md)
- [List Restore Jobs](actions/list-restore-jobs.md)
