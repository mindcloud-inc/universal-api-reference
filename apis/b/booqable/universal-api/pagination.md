# Booqable Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Booqable expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-product-availability?connectionId=$CONNECTION_ID&limit=25&offset=0&month=4&year=2026&productId=6774b37c-a832-4868-8ae9-b9c90cb5c75e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Booqable actions that support pagination

- [Get Product Availability](actions/get-product-availability.md)
- [List Customers](actions/list-customers.md)
- [List Items](actions/list-items.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Stock Items](actions/list-stock-items.md)
- [Search Customers](actions/search-customers.md)
- [Search Items](actions/search-items.md)
- [Search Orders](actions/search-orders.md)
- [Search Products](actions/search-products.md)
