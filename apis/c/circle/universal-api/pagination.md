# Circle Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Circle expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-access-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Circle actions that support pagination

- [List Access Groups](actions/list-access-groups.md)
- [List Basic Posts](actions/list-basic-posts.md)
- [List Comments](actions/list-comments.md)
- [List Community Member Spaces](actions/list-community-member-spaces.md)
- [List Community Members](actions/list-community-members.md)
- [List Community Segments](actions/list-community-segments.md)
- [List Events](actions/list-events.md)
- [List Member Tags](actions/list-member-tags.md)
- [List Profile Fields](actions/list-profile-fields.md)
- [List Space Members](actions/list-space-members.md)
- [List Spaces](actions/list-spaces.md)
- [List Topics](actions/list-topics.md)
- [Search Community Members](actions/search-community-members.md)
