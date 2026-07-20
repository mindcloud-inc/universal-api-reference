# Goodbarber eCommerce Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Goodbarber eCommerce expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Goodbarber eCommerce actions that support pagination

- [List Collections](actions/list-collections.md)
- [List Customers](actions/list-customers.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Prospects](actions/list-prospects.md)
- [List Tags](actions/list-tags.md)
- [List Variant Options](actions/list-variant-options.md)
