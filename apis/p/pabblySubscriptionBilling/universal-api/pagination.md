# Pabbly Subscription Billing Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pabbly Subscription Billing expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/affiliate-clicks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pabbly Subscription Billing actions that support pagination

- [Affiliate Clicks](actions/affiliate-clicks.md)
- [Affiliate Links](actions/affiliate-links.md)
- [Get License Codes](actions/get-license-codes.md)
- [List All Addon Categories By Product ID](actions/list-all-addon-categories-by-product-id.md)
- [List All Addons](actions/list-all-addons.md)
- [List All Coupons By Product](actions/list-all-coupons-by-product.md)
- [List All Customers](actions/list-all-customers.md)
- [List All Invoices](actions/list-all-invoices.md)
- [List All Invoices By Customer Id](actions/list-all-invoices-by-customer-id.md)
- [List All Licenses](actions/list-all-licenses.md)
- [List All Multiplans](actions/list-all-multiplans.md)
- [List All Payment Gateways](actions/list-all-payment-gateways.md)
- [List All Payment Methods By Customer Id](actions/list-all-payment-methods-by-customer-id.md)
- [List All Plans](actions/list-all-plans.md)
- [List All Plans By Product ID](actions/list-all-plans-by-product-id.md)
- [List All Product](actions/list-all-product.md)
- [List All Refund By Customer Id](actions/list-all-refund-by-customer-id.md)
- [List All Subscriptions](actions/list-all-subscriptions.md)
- [List All Subscriptions By Customer Id](actions/list-all-subscriptions-by-customer-id.md)
- [List All Transactions By Customer Id](actions/list-all-transactions-by-customer-id.md)
- [List All Transactions By Invoice Id](actions/list-all-transactions-by-invoice-id.md)
- [List Commissions](actions/list-commissions.md)
