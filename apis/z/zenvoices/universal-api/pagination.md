# Zenvoices Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zenvoices expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zenvoices actions that support pagination

- [List Accounts](actions/list-accounts.md)
- [List Administrations](actions/list-administrations.md)
- [List Cost Centres](actions/list-cost-centres.md)
- [List Cost Units](actions/list-cost-units.md)
- [List Employees](actions/list-employees.md)
- [List Financial Transactions](actions/list-financial-transactions.md)
- [List Inbox Documents](actions/list-inbox-documents.md)
- [List Ledger Accounts](actions/list-ledger-accounts.md)
- [List Payment Conditions](actions/list-payment-conditions.md)
- [List Products](actions/list-products.md)
- [List Projects](actions/list-projects.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Tax Codes](actions/list-tax-codes.md)
