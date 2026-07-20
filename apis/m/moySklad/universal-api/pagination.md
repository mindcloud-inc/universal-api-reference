# MoySklad Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model MoySklad expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-bundles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## MoySklad actions that support pagination

- [List bundles](actions/list-bundles.md)
- [List counterparties](actions/list-counterparties.md)
- [List countries](actions/list-countries.md)
- [List currencies](actions/list-currencies.md)
- [List customer orders](actions/list-customer-orders.md)
- [List demands](actions/list-demands.md)
- [List employees](actions/list-employees.md)
- [List groups](actions/list-groups.md)
- [List inventories](actions/list-inventories.md)
- [List invoices in](actions/list-invoices-in.md)
- [List invoices out](actions/list-invoices-out.md)
- [List moves](actions/list-moves.md)
- [List organizations](actions/list-organizations.md)
- [List payments in](actions/list-payments-in.md)
- [List payments out](actions/list-payments-out.md)
- [List product folders](actions/list-product-folders.md)
- [List products](actions/list-products.md)
- [List purchase orders](actions/list-purchase-orders.md)
- [List regions](actions/list-regions.md)
- [List services](actions/list-services.md)
- [List stores](actions/list-stores.md)
- [List supplies](actions/list-supplies.md)
- [List variants](actions/list-variants.md)
