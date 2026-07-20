# Taskade Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Taskade expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-folder-agents?connectionId=$CONNECTION_ID&limit=25&offset=0&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Taskade actions that support pagination

- [List Folder Agents](actions/list-folder-agents.md)
- [List Folder Media Files](actions/list-folder-media-files.md)
- [List Folder Project Templates](actions/list-folder-project-templates.md)
- [List My Projects](actions/list-my-projects.md)
- [List Project Members](actions/list-project-members.md)
