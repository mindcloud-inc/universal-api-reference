# TrainerCentral Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model TrainerCentral expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-academy-learners?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## TrainerCentral actions that support pagination

- [List Academy Learners](actions/list-academy-learners.md)
- [List Course Members](actions/list-course-members.md)
- [List Courses](actions/list-courses.md)
- [List Upcoming Sessions](actions/list-upcoming-sessions.md)
