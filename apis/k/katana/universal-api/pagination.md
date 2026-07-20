# Katana Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Katana expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-current-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Katana actions that support pagination

- [List Current Inventory](actions/list-current-inventory.md)
- [List Customers](actions/list-customers.md)
- [List Inventory Movements](actions/list-inventory-movements.md)
- [List Locations](actions/list-locations.md)
- [List Manufacturing Orders](actions/list-manufacturing-orders.md)
- [List Materials](actions/list-materials.md)
- [List Products](actions/list-products.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Sales Order Fulfillments](actions/list-sales-order-fulfillments.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Variants](actions/list-variants.md)
- [List Variants with Negative Stock](actions/list-variants-with-negative-stock.md)
