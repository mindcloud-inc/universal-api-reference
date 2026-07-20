# HelpSpace Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model HelpSpace expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## HelpSpace actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Docs Articles](actions/list-docs-articles.md)
- [List Docs Categories](actions/list-docs-categories.md)
- [List Docs Sites](actions/list-docs-sites.md)
- [List Tags](actions/list-tags.md)
- [List Tasks](actions/list-tasks.md)
- [List Ticket Messages](actions/list-ticket-messages.md)
- [List Tickets](actions/list-tickets.md)
