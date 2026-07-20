# SalesapCRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SalesapCRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SalesapCRM actions that support pagination

- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Diary Events](actions/list-diary-events.md)
- [List Diary Tasks](actions/list-diary-tasks.md)
- [List Invoices](actions/list-invoices.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
