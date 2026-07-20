# CheckFlow Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CheckFlow expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/find-checklists?connectionId=$CONNECTION_ID&limit=25&offset=0&templateKey=0e7ad584-7788-4ab1-95a6-ca0a5b444cbb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CheckFlow actions that support pagination

- [Find Checklists](actions/find-checklists.md)
- [Get Checklist Details](actions/get-checklist-details.md)
- [Get Uploaded Checklist Files](actions/get-uploaded-checklist-files.md)
- [List Tasks by Task Key](actions/list-tasks-by-task-key.md)
