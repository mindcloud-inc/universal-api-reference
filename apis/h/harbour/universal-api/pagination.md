# Harbour Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Harbour expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreement-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Harbour actions that support pagination

- [List Agreement Links](actions/list-agreement-links.md)
- [List Agreements](actions/list-agreements.md)
- [List Brands](actions/list-brands.md)
- [List Documents](actions/list-documents.md)
- [List Folders](actions/list-folders.md)
- [List Items](actions/list-items.md)
- [List Organizations](actions/list-organizations.md)
