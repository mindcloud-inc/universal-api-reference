# Instructure Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Instructure expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-activity-stream?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Instructure actions that support pagination

- [List Activity Stream](actions/list-activity-stream.md)
- [List Announcements](actions/list-announcements.md)
- [List Assignments](actions/list-assignments.md)
- [List Calendar Events](actions/list-calendar-events.md)
- [List Course Enrollments](actions/list-course-enrollments.md)
- [List Courses](actions/list-courses.md)
- [List Discussion Topics](actions/list-discussion-topics.md)
- [List Folder Files](actions/list-folder-files.md)
- [List Missing Submissions](actions/list-missing-submissions.md)
- [List Module Items](actions/list-module-items.md)
- [List Modules](actions/list-modules.md)
- [List Pages](actions/list-pages.md)
- [List Todo Items](actions/list-todo-items.md)
- [List Upcoming Events](actions/list-upcoming-events.md)
- [List User Folders](actions/list-user-folders.md)
