# ShopWired Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ShopWired expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ShopWired actions that support pagination

- [List active brands](actions/list-brands.md)
- [List categories](actions/list-categories.md)
- [List customers](actions/list-customers.md)
- [List filter groups](actions/list-filter-groups.md)
- [List incomplete orders](actions/list-incomplete-orders.md)
- [List newsletter subscribers](actions/list-newsletter-subscribers.md)
- [List order statuses](actions/list-order-statuses.md)
- [List orders](actions/list-orders.md)
- [List product reviews](actions/list-product-reviews.md)
- [List products](actions/list-products.md)
- [Search for orders](actions/search-orders.md)
- [Search products](actions/search-products.md)
