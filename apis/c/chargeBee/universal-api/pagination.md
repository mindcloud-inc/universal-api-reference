# ChargeBee Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ChargeBee expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-business-entities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ChargeBee actions that support pagination

- [List Business Entities](actions/list-business-entities.md)
- [List Coupons](actions/list-coupons.md)
- [List Credit Notes](actions/list-credit-notes.md)
- [List Customers](actions/list-customers.md)
- [List Events](actions/list-events.md)
- [List Hosted Pages](actions/list-hosted-pages.md)
- [List Invoices](actions/list-invoices.md)
- [List Item Prices](actions/list-item-prices.md)
- [List Items](actions/list-items.md)
- [List Orders](actions/list-orders.md)
- [List Payment Sources](actions/list-payment-sources.md)
- [List Promotional Credits](actions/list-promotional-credits.md)
- [List Quotes](actions/list-quotes.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
- [List Unbilled Charges](actions/list-unbilled-charges.md)
- [List Usages](actions/list-usages.md)
- [List Virtual Bank Accounts](actions/list-virtual-bank-accounts.md)
