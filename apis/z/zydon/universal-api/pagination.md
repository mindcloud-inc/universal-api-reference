# Zydon Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zydon expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zydon actions that support pagination

- [List Brands](actions/list-brands.md)
- [List Categories](actions/list-categories.md)
- [List Companies](actions/list-companies.md)
- [List Financials](actions/list-financials.md)
- [List Measure Units](actions/list-measure-units.md)
- [List Orders](actions/list-orders.md)
- [List Partners](actions/list-partners.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Price Tables](actions/list-price-tables.md)
- [List Products](actions/list-products.md)
- [List Profiles](actions/list-profiles.md)
- [List Sales](actions/list-sales.md)
- [List Sellers](actions/list-sellers.md)
- [List Variations](actions/list-variations.md)
- [List Warehouses](actions/list-warehouses.md)
