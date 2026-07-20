# MS SharePoint Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model MS SharePoint expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-drive-root-items?connectionId=$CONNECTION_ID&limit=25&offset=0&driveId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## MS SharePoint actions that support pagination

- [List Drive Root Items](actions/list-drive-root-items.md)
- [List Folder Items](actions/list-folder-items.md)
- [List List Columns](actions/list-list-columns.md)
- [List List Items](actions/list-list-items.md)
- [List Site Drives](actions/list-site-drives.md)
- [List Site Lists](actions/list-site-lists.md)
- [List Subsites](actions/list-subsites.md)
- [Search Drive Items](actions/search-drive-items.md)
- [Search Sites](actions/search-sites.md)
