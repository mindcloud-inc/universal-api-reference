# Shopify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Shopify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/graphql-get-records-paginated?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Shopify actions that support pagination

- [GraphQL - Get Records (Paginated)](actions/graphql-get-records-paginated.md)
- [List All Orders](actions/list-all-orders-graphql.md)
- [List Companies](actions/list-companies-graphql.md)
- [List Customers](actions/list-customers-graphql.md)
- [List Deleted Product Events](actions/list-deleted-product-events.md)
- [List Locations](actions/list-locations.md)
- [List Orders](actions/list-orders.md)
- [List Product Variants](actions/list-product-variants.md)
- [List Products](actions/list-products.md)
