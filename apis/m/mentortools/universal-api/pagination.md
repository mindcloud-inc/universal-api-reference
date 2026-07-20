# Mentortools Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mentortools expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-course-module-lessons?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mentortools actions that support pagination

- [List Course Module Lessons](actions/list-course-module-lessons.md)
- [List Course Modules](actions/list-course-modules.md)
- [List Courses](actions/list-courses.md)
- [List Module Submodules](actions/list-module-submodules.md)
