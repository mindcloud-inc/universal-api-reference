# Global Payments WebPay Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Global Payments WebPay expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction-summary-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Global Payments WebPay actions that support pagination

- [Get Transaction Summary Report](actions/get-transaction-summary-report.md)
- [List Accounts](actions/list-accounts.md)
- [List Disputes](actions/list-disputes.md)
- [List Links](actions/list-links.md)
- [List Merchants](actions/list-merchants.md)
- [List Payers](actions/list-payers.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Settled Disputes](actions/list-settled-disputes.md)
- [List Settled Transactions](actions/list-settled-transactions.md)
- [List Settlement Deposits](actions/list-settlement-deposits.md)
- [List Transactions](actions/list-transactions.md)
- [Search Payment Methods](actions/search-payment-methods.md)
