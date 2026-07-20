# Polymer Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Polymer expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/list-active-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Polymer actions that support pagination

- [List Active Users](actions/list-active-users.md)
- [List Candidates](actions/list-candidates.md)
- [List Deactivated Users](actions/list-deactivated-users.md)
- [List Job Applications](actions/list-job-applications.md)
- [List Jobs](actions/list-jobs.md)
