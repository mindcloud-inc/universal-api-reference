# Reach360 Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Reach360 expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-activity-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Reach360 actions that support pagination

- [Get Activity Report](actions/get-activity-report.md)
- [Get Course Report](actions/get-course-report.md)
- [Get Learner Report](actions/get-learner-report.md)
- [Get Learning Path Courses Report](actions/get-learning-path-courses-report.md)
- [Get Learning Path Learners Report](actions/get-learning-path-learners-report.md)
- [List Courses](actions/list-courses.md)
- [List Group Users](actions/list-group-users.md)
- [List Groups](actions/list-groups.md)
- [List Invitations](actions/list-invitations.md)
- [List Learning Path Courses](actions/list-learning-path-courses.md)
- [List Learning Paths](actions/list-learning-paths.md)
- [List User Groups](actions/list-user-groups.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
