# Thinkific Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Thinkific expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-course-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Thinkific actions that support pagination

- [List Course Reviews](actions/list-course-reviews.md)
- [List Courses](actions/list-courses.md)
- [List Enrollments](actions/list-enrollments.md)
- [List Groups](actions/list-groups.md)
- [List Instructors](actions/list-instructors.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Site Scripts](actions/list-site-scripts.md)
- [List Users](actions/list-users.md)
