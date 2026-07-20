# Visma eAccounting Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Visma eAccounting expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Visma eAccounting actions that support pagination

- [List Articles](actions/list-articles.md)
- [List Customer Invoice Drafts](actions/list-customer-invoice-drafts.md)
- [List Customer Invoices](actions/list-customer-invoices.md)
- [List Customers](actions/list-customers.md)
- [List Orders](actions/list-orders.md)
- [List Quotes](actions/list-quotes.md)
