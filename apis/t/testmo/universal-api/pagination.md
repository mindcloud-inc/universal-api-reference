# Testmo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Testmo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/list-automation-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Testmo actions that support pagination

- [List Automation Runs](actions/list-automation-runs.md)
- [List Automation Sources](actions/list-automation-sources.md)
- [List Case Attachments](actions/list-case-attachments.md)
- [List Cases](actions/list-cases.md)
- [List Folders](actions/list-folders.md)
- [List Milestones](actions/list-milestones.md)
- [List Project Users](actions/list-project-users.md)
- [List Projects](actions/list-projects.md)
- [List Runs](actions/list-runs.md)
- [List Sessions](actions/list-sessions.md)
- [List Users](actions/list-users.md)
