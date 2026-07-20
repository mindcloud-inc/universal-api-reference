# Emporix Commerce Engine Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Emporix Commerce Engine expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Emporix Commerce Engine actions that support pagination

- [List Brands](actions/list-brands.md)
- [List Carts](actions/list-carts.md)
- [List Catalogs](actions/list-catalogs.md)
- [List Categories](actions/list-categories.md)
- [List Category Trees](actions/list-category-trees.md)
- [List Labels](actions/list-labels.md)
- [List Legal Entities](actions/list-legal-entities.md)
- [List Price Lists](actions/list-price-lists.md)
- [List Prices](actions/list-prices.md)
- [List Product Templates](actions/list-product-templates.md)
- [List Products](actions/list-products.md)
- [List Sales Orders](actions/list-sales-orders.md)
