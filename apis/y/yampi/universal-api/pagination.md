# Yampi Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Yampi expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Yampi actions that support pagination

- [List Brands](actions/list-brands.md)
- [List Categories](actions/list-categories.md)
- [List Category Products](actions/list-category-products.md)
- [List Customer Addresses](actions/list-customer-addresses.md)
- [List Customer Carts](actions/list-customer-carts.md)
- [List Customers](actions/list-customers.md)
- [List Customizations](actions/list-customizations.md)
- [List Leads](actions/list-leads.md)
- [List Order Addresses](actions/list-order-addresses.md)
- [List Order Items](actions/list-order-items.md)
- [List Orders](actions/list-orders.md)
- [List Product Combos](actions/list-product-combos.md)
- [List Product Comments](actions/list-product-comments.md)
- [List Product Promotions](actions/list-product-promotions.md)
- [List Product Reviews](actions/list-product-reviews.md)
- [List Product SKUs](actions/list-product-skus.md)
- [List Product Stocks](actions/list-product-stocks.md)
- [List Products](actions/list-products.md)
