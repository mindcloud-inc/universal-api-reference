# QuickBooks Online Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model QuickBooks Online expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0&query=select%20*%20from%20Account%20where%20AccountType%20%3D%20'Expense'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## QuickBooks Online actions that support pagination

- [List Accounts](actions/list-accounts.md)
- [List Bills](actions/list-bills.md)
- [List Budgets](actions/list-budgets.md)
- [List Customers](actions/list-customers.md)
- [List Invoices](actions/list-invoices.md)
- [List Items](actions/list-items.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Sales Receipts](actions/list-sales-receipts.md)
- [List Vendors](actions/list-vendors.md)
- [Query](actions/query.md)
