# Webling Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Webling expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Webling actions that support pagination

- [List Articles](actions/list-articles.md)
- [List Debitors](actions/list-debitors.md)
- [List Documentgroups](actions/list-documentgroups.md)
- [List Documents](actions/list-documents.md)
- [List Entries](actions/list-entries.md)
- [List Entrygroups](actions/list-entrygroups.md)
- [List Membergroups](actions/list-membergroups.md)
- [List Members](actions/list-members.md)
- [List Users](actions/list-users.md)
