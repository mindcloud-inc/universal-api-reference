# Userback Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Userback expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-feedback-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Userback actions that support pagination

- [List Feedback Comments](actions/list-feedback-comments.md)
- [List Feedbacks](actions/list-feedbacks.md)
- [List Members](actions/list-members.md)
- [List Session Recordings](actions/list-session-recordings.md)
- [List Workflows](actions/list-workflows.md)
