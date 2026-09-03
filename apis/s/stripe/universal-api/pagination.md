# Stripe Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Stripe expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Stripe actions that support pagination

- [List Charges](actions/list-charges.md)
- [List Checkout Session Line Items](actions/list-checkout-session-line-items.md)
- [List Checkout Sessions](actions/list-checkout-sessions.md)
- [List Credit Notes](actions/list-credit-notes.md)
- [List Customer Payment Methods](actions/list-customer-payment-methods.md)
- [List Customers](actions/list-customers.md)
- [List Disputes](actions/list-disputes.md)
- [List Events](actions/list-events.md)
- [List Invoice Line Items](actions/list-invoice-line-items.md)
- [List Payment Intents](actions/list-payment-intents.md)
- [List Prices](actions/list-prices.md)
- [List Products](actions/list-products.md)
- [List Refunds](actions/list-refunds.md)
- [List Subscription Schedules](actions/list-subscription-schedules.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [Search Customers](actions/search-customers.md)
- [Search Payment Intents](actions/search-payment-intents.md)
