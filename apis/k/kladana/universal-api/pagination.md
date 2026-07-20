# Kladana Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Kladana expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-assortment?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Kladana actions that support pagination

- [List Assortment](actions/list-assortment.md)
- [List Batches](actions/list-batches.md)
- [List Bundles](actions/list-bundles.md)
- [List Contracts](actions/list-contracts.md)
- [List Counterparties](actions/list-counterparties.md)
- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Employees](actions/list-employees.md)
- [List Incoming Payments](actions/list-incoming-payments.md)
- [List Inventory Counts](actions/list-inventory-counts.md)
- [List Organizations](actions/list-organizations.md)
- [List Outgoing Payments](actions/list-outgoing-payments.md)
- [List Product Groups](actions/list-product-groups.md)
- [List Product Variants](actions/list-product-variants.md)
- [List Products](actions/list-products.md)
- [List Projects](actions/list-projects.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Receivings](actions/list-receivings.md)
- [List Sales Invoices](actions/list-sales-invoices.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Services](actions/list-services.md)
- [List Shipments](actions/list-shipments.md)
- [List Supplier Invoices](actions/list-supplier-invoices.md)
- [List Units Of Measure](actions/list-units-of-measure.md)
- [List Warehouses](actions/list-warehouses.md)
