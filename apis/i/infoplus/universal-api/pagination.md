# Infoplus Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Infoplus expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-aisles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Infoplus actions that support pagination

- [Search Aisles](actions/search-aisles.md)
- [Search ASNs](actions/search-asns.md)
- [Search Bills of Lading](actions/search-bills-of-lading.md)
- [Search Buildings](actions/search-buildings.md)
- [Search Carton Activities](actions/search-carton-activities.md)
- [Search Carton Contents](actions/search-carton-contents.md)
- [Search Cartons](actions/search-cartons.md)
- [Search Customers](actions/search-customers.md)
- [Search External Shipments](actions/search-external-shipments.md)
- [Search Fulfillment Plans](actions/search-fulfillment-plans.md)
- [Search Fulfillment Processes](actions/search-fulfillment-processes.md)
- [Search Inventory Adjustments](actions/search-inventory-adjustments.md)
- [Search Inventory Details](actions/search-inventory-details.md)
- [Search Inventory Snapshots](actions/search-inventory-snapshots.md)
- [Search Inventory Storage Activities](actions/search-inventory-storage-activities.md)
- [Search Item Activities](actions/search-item-activities.md)
- [Search Item Receipt Activities](actions/search-item-receipt-activities.md)
- [Search Item Receipts](actions/search-item-receipts.md)
- [Search Items](actions/search-items.md)
- [Search Kits](actions/search-kits.md)
- [Search Lines of Business](actions/search-lines-of-business.md)
- [Search Load Contents](actions/search-load-contents.md)
- [Search Loads](actions/search-loads.md)
- [Search Location Footprints](actions/search-location-footprints.md)
- [Search Locations](actions/search-locations.md)
- [Search Low Stock Records](actions/search-low-stock-records.md)
- [Search Order Activities](actions/search-order-activities.md)
- [Search Order Lines](actions/search-order-lines.md)
- [Search Order Sources](actions/search-order-sources.md)
- [Search Orders](actions/search-orders.md)
- [Search Parcel Invoices](actions/search-parcel-invoices.md)
- [Search Receiving Processes](actions/search-receiving-processes.md)
- [Search Receiving Worksheets](actions/search-receiving-worksheets.md)
- [Search Replenishment Plans](actions/search-replenishment-plans.md)
- [Search Replenishments](actions/search-replenishments.md)
- [Search Return Shipments](actions/search-return-shipments.md)
- [Search Shipments](actions/search-shipments.md)
- [Search Vendors](actions/search-vendors.md)
- [Search Warehouses](actions/search-warehouses.md)
- [Search Zones](actions/search-zones.md)
