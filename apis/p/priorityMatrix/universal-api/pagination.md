# Priority Matrix Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Priority Matrix expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-items-by-date?connectionId=$CONNECTION_ID&limit=25&offset=0&creationDateGt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Priority Matrix actions that support pagination

- [Find Items By Date](actions/find-items-by-date.md)
- [Find Items By Tag](actions/find-items-by-tag.md)
- [Find Projects By Creation Date](actions/find-projects-by-creation-date.md)
- [Find Projects By Schedule Date](actions/find-projects-by-schedule-date.md)
- [Find Projects By Tag](actions/find-projects-by-tag.md)
- [List Account Members](actions/list-account-members.md)
- [List Active Projects](actions/list-active-projects.md)
- [List Collaborators](actions/list-collaborators.md)
- [List Completed Project Items](actions/list-completed-project-items.md)
- [List Inbox Items](actions/list-inbox-items.md)
- [List Items](actions/list-items.md)
- [List Project Item Summaries](actions/list-project-item-summaries.md)
- [List Project Items](actions/list-project-items.md)
- [List Project Items By Quadrant](actions/list-project-items-by-quadrant.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
