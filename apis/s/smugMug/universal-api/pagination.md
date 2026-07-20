# SmugMug Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SmugMug expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/list-album-images?connectionId=$CONNECTION_ID&limit=25&offset=0&albumKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SmugMug actions that support pagination

- [List Album Images](actions/list-album-images.md)
- [List Album Popular Media](actions/list-album-popular-media.md)
- [List Child Nodes](actions/list-child-nodes.md)
- [List Folder Albums](actions/list-folder-albums.md)
- [List Folder Folders](actions/list-folder-folders.md)
- [List Parent Nodes](actions/list-parent-nodes.md)
- [List User Albums](actions/list-user-albums.md)
- [List User Popular Media](actions/list-user-popular-media.md)
- [List User Recent Images](actions/list-user-recent-images.md)
