# MindCloud Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model MindCloud expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-failed-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## MindCloud actions that support pagination

- [List Failed Runs](actions/list-failed-runs.md)
- [List Run Operations](actions/list-run-operations.md)
- [List Workflow Activity](actions/list-workflow-activity.md)
- [List Workflow Runs](actions/list-workflow-runs.md)
