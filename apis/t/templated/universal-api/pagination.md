# Templated Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Templated expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-folder-templates?connectionId=$CONNECTION_ID&limit=25&offset=0&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Templated actions that support pagination

- [List Folder Templates](actions/list-folder-templates.md)
- [List Folders](actions/list-folders.md)
- [List Gallery Templates](actions/list-gallery-templates.md)
- [List Template Renders](actions/list-template-renders.md)
- [List Templates](actions/list-templates.md)
