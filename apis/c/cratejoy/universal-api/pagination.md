# Cratejoy Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cratejoy expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customer-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cratejoy actions that support pagination

- [List Customer Addresses](actions/list-customer-addresses.md)
- [List Customers](actions/list-customers.md)
- [List Inventory Levels](actions/list-inventory-levels.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Shipments](actions/list-shipments.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
