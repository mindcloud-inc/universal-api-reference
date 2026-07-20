# Zendesk Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zendesk expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/execute-view?connectionId=$CONNECTION_ID&limit=25&offset=0&view_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zendesk actions that support pagination

- [Execute View](actions/execute-view.md)
- [List Group Memberships](actions/list-group-memberships.md)
- [List Groups](actions/list-groups.md)
- [List Organization Memberships](actions/list-organization-memberships.md)
- [List Organizations](actions/list-organizations.md)
- [List Ticket Audits](actions/list-ticket-audits.md)
- [List Ticket Comments](actions/list-ticket-comments.md)
- [List Ticket Fields](actions/list-ticket-fields.md)
- [List Ticket Forms](actions/list-ticket-forms.md)
- [List Tickets](actions/list-tickets.md)
- [List Users](actions/list-users.md)
- [List Views](actions/list-views.md)
- [Search](actions/search.md)
- [Search Users](actions/search-users.md)
