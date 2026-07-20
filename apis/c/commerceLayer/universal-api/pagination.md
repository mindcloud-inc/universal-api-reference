# Commerce Layer Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Commerce Layer expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Commerce Layer actions that support pagination

- [List Addresses](actions/list-addresses.md)
- [List Inventory Models](actions/list-inventory-models.md)
- [List Manual Tax Calculators](actions/list-manual-tax-calculators.md)
- [List Markets](actions/list-markets.md)
- [List Merchants](actions/list-merchants.md)
- [List Price Lists](actions/list-price-lists.md)
- [List Shipping Categories](actions/list-shipping-categories.md)
- [List Stock Locations](actions/list-stock-locations.md)
- [List Tax Categories](actions/list-tax-categories.md)
- [List Tax Rules](actions/list-tax-rules.md)
