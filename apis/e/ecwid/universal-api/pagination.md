# Ecwid Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Ecwid expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-abandoned-carts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Ecwid actions that support pagination

- [Search Abandoned Carts](actions/search-abandoned-carts.md)
- [Search Categories](actions/search-categories.md)
- [Search Customers](actions/search-customers.md)
- [Search Discount Coupons](actions/search-discount-coupons.md)
- [Search Orders](actions/search-orders.md)
- [Search Product Brands](actions/search-product-brands.md)
- [Search Products](actions/search-products.md)
