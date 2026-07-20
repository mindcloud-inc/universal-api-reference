# Request Tracker (RT) Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Request Tracker (RT) expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-group-members?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Request Tracker (RT) actions that support pagination

- [Get Group Members](actions/get-group-members.md)
- [Get Ticket Attachments](actions/get-ticket-attachments.md)
- [Get Ticket History](actions/get-ticket-history.md)
- [Get User Groups](actions/get-user-groups.md)
- [List Queues](actions/list-queues.md)
- [Search Groups](actions/search-groups.md)
- [Search Queues](actions/search-queues.md)
- [Search Tickets](actions/search-tickets.md)
- [Search Users](actions/search-users.md)
