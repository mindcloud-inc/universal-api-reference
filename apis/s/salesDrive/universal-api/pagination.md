# SalesDrive Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SalesDrive expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-acts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SalesDrive actions that support pagination

- [List Acts](actions/list-acts.md)
- [List Cash Orders](actions/list-cash-orders.md)
- [List Checks](actions/list-checks.md)
- [List Contracts](actions/list-contracts.md)
- [List Invoices](actions/list-invoices.md)
- [List Orders](actions/list-orders.md)
- [List Payments](actions/list-payments.md)
- [List Product Arrivals](actions/list-product-arrivals.md)
- [List Sales Invoices](actions/list-sales-invoices.md)
