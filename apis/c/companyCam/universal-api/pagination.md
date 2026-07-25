# CompanyCam Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CompanyCam expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-all-checklists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CompanyCam actions that support pagination

- [List All Checklists](actions/list-all-checklists.md)
- [List Groups](actions/list-groups.md)
- [List Photo Comments](actions/list-photo-comments.md)
- [List Photo Tags](actions/list-photo-tags.md)
- [List Photos](actions/list-photos.md)
- [List Project Comments](actions/list-project-comments.md)
- [List Project Documents](actions/list-project-documents.md)
- [List Project Labels](actions/list-project-labels.md)
- [List Project Photos](actions/list-project-photos.md)
- [List Project Users](actions/list-project-users.md)
- [List Project Videos](actions/list-project-videos.md)
- [List Projects](actions/list-projects.md)
- [List Tags](actions/list-tags.md)
- [List Users](actions/list-users.md)
- [List Videos](actions/list-videos.md)
