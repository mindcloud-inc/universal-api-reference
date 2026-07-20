# Crowdin Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Crowdin expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-project-progress?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Crowdin actions that support pagination

- [Get Project Progress](actions/get-project-progress.md)
- [List Branches](actions/list-branches.md)
- [List Directories](actions/list-directories.md)
- [List File Revisions](actions/list-file-revisions.md)
- [List Files](actions/list-files.md)
- [List Project Builds](actions/list-project-builds.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
- [List Supported Languages](actions/list-supported-languages.md)
