# Dukaan Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Dukaan expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-discounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Dukaan actions that support pagination

- [List Discounts](actions/list-discounts.md)
- [List Inventory Products](actions/list-inventory-products.md)
- [List Orders](actions/list-orders.md)
- [List Product Categories](actions/list-product-categories.md)
- [List Products](actions/list-products.md)
- [List Products By Category](actions/list-products-by-category.md)
- [List Store Audience](actions/list-store-audience.md)
- [List Warehouses](actions/list-warehouses.md)
- [Search Orders](actions/search-orders.md)
- [Search Product Categories](actions/search-product-categories.md)
- [Search Products](actions/search-products.md)
