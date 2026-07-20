# Assembly.com Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Assembly.com expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Assembly.com actions that support pagination

- [List Clients](actions/list-clients.md)
- [List Companies](actions/list-companies.md)
- [List Invoices](actions/list-invoices.md)
- [List Message Channels](actions/list-message-channels.md)
- [List Messages](actions/list-messages.md)
- [List Notes](actions/list-notes.md)
- [List Payments](actions/list-payments.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Tasks](actions/list-tasks.md)
