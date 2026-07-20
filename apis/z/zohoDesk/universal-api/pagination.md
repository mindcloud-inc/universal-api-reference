# Zoho Desk Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho Desk expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-layouts?connectionId=$CONNECTION_ID&limit=25&offset=0&module=tickets&status=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho Desk actions that support pagination

- [List Layouts](actions/list-layouts.md)
- [List Tickets](actions/list-tickets.md)
- [Search Accounts](actions/search-accounts.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Tickets](actions/search-tickets.md)
