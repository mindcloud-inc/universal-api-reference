# Mural Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mural expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-default-and-custom-templates-for-workspace?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mural actions that support pagination

- [List Default and Custom Templates for Workspace](actions/list-default-and-custom-templates-for-workspace.md)
- [List Folders for Room](actions/list-folders-for-room.md)
- [List Murals for Room](actions/list-murals-for-room.md)
- [List Murals for Workspace](actions/list-murals-for-workspace.md)
- [List Open Rooms for Workspace](actions/list-open-rooms-for-workspace.md)
- [List Recent Templates for Workspace](actions/list-recent-templates-for-workspace.md)
- [List Recently Opened Murals for Workspace](actions/list-recently-opened-murals-for-workspace.md)
- [List Rooms for Workspace](actions/list-rooms-for-workspace.md)
- [List Workspaces](actions/list-workspaces.md)
