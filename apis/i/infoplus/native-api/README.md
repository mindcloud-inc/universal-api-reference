# Infoplus: Native API Reference

A consolidated summary of Infoplus's API configuration and 115 documented operations, with links to official documentation.

- **Official docs:** https://developer.infopluscommerce.com/api/reference/v3.0/
- **OpenAPI specification:** https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json
- **API base URL:** `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`

## Authentication

### API Key

Authenticate Infoplus requests with the API-Key HTTP header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.infopluscommerce.com/api/reference/swagger-ui/v1/introduction.html#authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `in`, `like`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `!` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (115 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Aisle](actions/create-aisle.md) | `POST /aisle` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create ASN](actions/create-asn.md) | `POST /asn` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Bill of Lading](actions/create-bill-of-lading.md) | `POST /billOfLading` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Building](actions/create-building.md) | `POST /building` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Carton](actions/create-carton.md) | `POST /carton` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Carton Activity](actions/create-carton-activity.md) | `POST /cartonActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Carton Content](actions/create-carton-content.md) | `POST /cartonContent` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create External Shipment](actions/create-external-shipment.md) | `POST /externalShipment` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Fulfillment Plan](actions/create-fulfillment-plan.md) | `POST /fulfillmentPlan` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Inventory Storage Activity](actions/create-inventory-storage-activity.md) | `POST /inventoryStorageActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Item](actions/create-item.md) | `POST /item` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Item Receipt Activity](actions/create-item-receipt-activity.md) | `POST /itemReceiptActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Kit](actions/create-kit.md) | `POST /kit` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Line of Business](actions/create-line-of-business.md) | `POST /lineOfBusiness` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Location](actions/create-location.md) | `POST /location` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Location Footprint](actions/create-location-footprint.md) | `POST /locationFootprint` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Order](actions/create-order.md) | `POST /order` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Order Activity](actions/create-order-activity.md) | `POST /orderActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Order Source](actions/create-order-source.md) | `POST /orderSource` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Receiving Worksheet](actions/create-receiving-worksheet.md) | `POST /receivingWorksheet` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Replenishment Plan](actions/create-replenishment-plan.md) | `POST /replenishmentPlan` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Vendor](actions/create-vendor.md) | `POST /vendor` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Warehouse](actions/create-warehouse.md) | `POST /warehouse` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Create Zone](actions/create-zone.md) | `POST /zone` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Aisle](actions/delete-aisle.md) | `DELETE /aisle/{aisleId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete ASN](actions/delete-asn.md) | `DELETE /asn/{asnId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Bill of Lading](actions/delete-bill-of-lading.md) | `DELETE /billOfLading/{billOfLadingId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Building](actions/delete-building.md) | `DELETE /building/{buildingId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Carton](actions/delete-carton.md) | `DELETE /carton/{cartonId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Carton Activity](actions/delete-carton-activity.md) | `DELETE /cartonActivity/{cartonActivityId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Carton Content](actions/delete-carton-content.md) | `DELETE /cartonContent/{cartonContentId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customer/{customerId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete External Shipment](actions/delete-external-shipment.md) | `DELETE /externalShipment/{externalShipmentId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Fulfillment Plan](actions/delete-fulfillment-plan.md) | `DELETE /fulfillmentPlan/{fulfillmentPlanId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Inventory Storage Activity](actions/delete-inventory-storage-activity.md) | `DELETE /inventoryStorageActivity/{inventoryStorageActivityId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Item](actions/delete-item.md) | `DELETE /item/{itemId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Item Receipt Activity](actions/delete-item-receipt-activity.md) | `DELETE /itemReceiptActivity/{itemReceiptActivityId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Kit](actions/delete-kit.md) | `DELETE /kit/{kitId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Location](actions/delete-location.md) | `DELETE /location/{locationId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Location Footprint](actions/delete-location-footprint.md) | `DELETE /locationFootprint/{locationFootprintId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Order](actions/delete-order.md) | `DELETE /order/{orderId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Order Activity](actions/delete-order-activity.md) | `DELETE /orderActivity/{orderActivityId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Order Source](actions/delete-order-source.md) | `DELETE /orderSource/{orderSourceId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Parcel Invoice](actions/delete-parcel-invoice.md) | `DELETE /parcelInvoice/{parcelInvoiceId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Receiving Worksheet](actions/delete-receiving-worksheet.md) | `DELETE /receivingWorksheet/{receivingWorksheetId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Replenishment Plan](actions/delete-replenishment-plan.md) | `DELETE /replenishmentPlan/{replenishmentPlanId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Vendor](actions/delete-vendor.md) | `DELETE /vendor/{vendorId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Delete Zone](actions/delete-zone.md) | `DELETE /zone/{zoneId}` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Search Aisles](actions/search-aisles.md) | `GET /aisle/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search ASNs](actions/search-asns.md) | `GET /asn/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Bills of Lading](actions/search-bills-of-lading.md) | `GET /billOfLading/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Buildings](actions/search-buildings.md) | `GET /building/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Carton Activities](actions/search-carton-activities.md) | `GET /cartonActivity/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Carton Contents](actions/search-carton-contents.md) | `GET /cartonContent/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Cartons](actions/search-cartons.md) | `GET /carton/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Customers](actions/search-customers.md) | `GET /customer/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search External Shipments](actions/search-external-shipments.md) | `GET /externalShipment/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Fulfillment Plans](actions/search-fulfillment-plans.md) | `GET /fulfillmentPlan/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Fulfillment Processes](actions/search-fulfillment-processes.md) | `GET /fulfillmentProcess/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Inventory Adjustments](actions/search-inventory-adjustments.md) | `GET /inventoryAdjustment/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Inventory Details](actions/search-inventory-details.md) | `GET /inventoryDetail/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Inventory Snapshots](actions/search-inventory-snapshots.md) | `GET /inventorySnapshot/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Inventory Storage Activities](actions/search-inventory-storage-activities.md) | `GET /inventoryStorageActivity/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Item Activities](actions/search-item-activities.md) | `GET /itemActivity/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Item Receipt Activities](actions/search-item-receipt-activities.md) | `GET /itemReceiptActivity/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Item Receipts](actions/search-item-receipts.md) | `GET /itemReceipt/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Items](actions/search-items.md) | `GET /item/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Kits](actions/search-kits.md) | `GET /kit/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Lines of Business](actions/search-lines-of-business.md) | `GET /lineOfBusiness/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Load Contents](actions/search-load-contents.md) | `GET /loadContent/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Loads](actions/search-loads.md) | `GET /load/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Location Footprints](actions/search-location-footprints.md) | `GET /locationFootprint/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Locations](actions/search-locations.md) | `GET /location/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Low Stock Records](actions/search-low-stock-records.md) | `GET /lowStock/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Order Activities](actions/search-order-activities.md) | `GET /orderActivity/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Order Lines](actions/search-order-lines.md) | `GET /orderLine/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Order Sources](actions/search-order-sources.md) | `GET /orderSource/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Orders](actions/search-orders.md) | `GET /order/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Parcel Invoices](actions/search-parcel-invoices.md) | `GET /parcelInvoice/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Receiving Processes](actions/search-receiving-processes.md) | `GET /receivingProcess/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Receiving Worksheets](actions/search-receiving-worksheets.md) | `GET /receivingWorksheet/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Replenishment Plans](actions/search-replenishment-plans.md) | `GET /replenishmentPlan/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Replenishments](actions/search-replenishments.md) | `GET /replenishment/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Return Shipments](actions/search-return-shipments.md) | `GET /returnShipment/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Shipments](actions/search-shipments.md) | `GET /shipment/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Vendors](actions/search-vendors.md) | `GET /vendor/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Warehouses](actions/search-warehouses.md) | `GET /warehouse/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Search Zones](actions/search-zones.md) | `GET /zone/search` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/) |
| [Update Aisle](actions/update-aisle.md) | `PUT /aisle` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update ASN](actions/update-asn.md) | `PUT /asn` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Bill of Lading](actions/update-bill-of-lading.md) | `PUT /billOfLading` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Building](actions/update-building.md) | `PUT /building` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Carton](actions/update-carton.md) | `PUT /carton` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Carton Activity](actions/update-carton-activity.md) | `PUT /cartonActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Carton Content](actions/update-carton-content.md) | `PUT /cartonContent` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Customer](actions/update-customer.md) | `PUT /customer` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update External Shipment](actions/update-external-shipment.md) | `PUT /externalShipment` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Fulfillment Plan](actions/update-fulfillment-plan.md) | `PUT /fulfillmentPlan` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Inventory Storage Activity](actions/update-inventory-storage-activity.md) | `PUT /inventoryStorageActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Item](actions/update-item.md) | `PUT /item` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Item Receipt](actions/update-item-receipt.md) | `PUT /itemReceipt` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Item Receipt Activity](actions/update-item-receipt-activity.md) | `PUT /itemReceiptActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Kit](actions/update-kit.md) | `PUT /kit` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Line of Business](actions/update-line-of-business.md) | `PUT /lineOfBusiness` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Location](actions/update-location.md) | `PUT /location` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Location Footprint](actions/update-location-footprint.md) | `PUT /locationFootprint` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Order](actions/update-order.md) | `PUT /order` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Order Activity](actions/update-order-activity.md) | `PUT /orderActivity` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Order Source](actions/update-order-source.md) | `PUT /orderSource` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Receiving Worksheet](actions/update-receiving-worksheet.md) | `PUT /receivingWorksheet` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Replenishment Plan](actions/update-replenishment-plan.md) | `PUT /replenishmentPlan` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Vendor](actions/update-vendor.md) | `PUT /vendor` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Warehouse](actions/update-warehouse.md) | `PUT /warehouse` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
| [Update Zone](actions/update-zone.md) | `PUT /zone` | [docs](https://developer.infopluscommerce.com/api/reference/v3.0/swagger.json) |
