# eBay Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model eBay expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-offers?connectionId=$CONNECTION_ID&limit=25&offset=0&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## eBay actions that support pagination

- [List Offers by SKU](actions/get-offers.md)
- [Get Order](actions/get-order.md)
- [Get Seller Events](actions/get-seller-events.md)
- [List Inventory Items](actions/list-inventory-items.md)
- [List Inventory Locations](actions/list-inventory-locations.md)
- [List Orders](actions/list-orders.md)
- [List Payout Transactions](actions/list-payout-transactions.md)
- [List Payouts](actions/list-payouts.md)
- [List Seller Items](actions/list-seller-items.md)
- [List Seller Items_v2](actions/list-seller-items-v2.md)
