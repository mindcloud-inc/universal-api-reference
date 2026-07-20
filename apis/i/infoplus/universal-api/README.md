# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-22-as-15_1776881336551.png" alt="Infoplus logo" width="28" height="28"> Infoplus: Universal API

Infoplus WMS API wrapper for warehouse operations, inventory, orders, shipments, receiving, fulfillment, and supporting reference data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/infoplus/latest
- **Category:** Commerce
- **Actions:** 115
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.infopluscommerce.com
- **Vendor API docs:** https://developer.infopluscommerce.com/api/reference/v3.0/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Items](actions/search-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (115)

### Aisle

| Action | Method | Description |
| --- | --- | --- |
| [Create Aisle](actions/create-aisle.md) | POST | Creates a new aisle in Infoplus. |
| [Delete Aisle](actions/delete-aisle.md) | DELETE | Deletes an existing aisle from Infoplus. |
| [Search Aisles](actions/search-aisles.md) | GET | Finds matching aisles in Infoplus. |
| [Update Aisle](actions/update-aisle.md) | PUT | Updates an existing aisle in Infoplus. |

### Asn

| Action | Method | Description |
| --- | --- | --- |
| [Create ASN](actions/create-asn.md) | POST | Creates a new ASN in Infoplus. |
| [Delete ASN](actions/delete-asn.md) | DELETE | Deletes an existing ASN from Infoplus. |
| [Search ASNs](actions/search-asns.md) | GET | Finds matching ASNs in Infoplus. |
| [Update ASN](actions/update-asn.md) | PUT | Updates an existing ASN in Infoplus. |

### Bill Of Lading

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill of Lading](actions/create-bill-of-lading.md) | POST | Creates a new bill of lading in Infoplus. |
| [Delete Bill of Lading](actions/delete-bill-of-lading.md) | DELETE | Deletes an existing bill of lading from Infoplus. |
| [Search Bills of Lading](actions/search-bills-of-lading.md) | GET | Finds matching bills of lading in Infoplus. |
| [Update Bill of Lading](actions/update-bill-of-lading.md) | PUT | Updates an existing bill of lading in Infoplus. |

### Building

| Action | Method | Description |
| --- | --- | --- |
| [Create Building](actions/create-building.md) | POST | Creates a new building in Infoplus. |
| [Delete Building](actions/delete-building.md) | DELETE | Deletes an existing building from Infoplus. |
| [Search Buildings](actions/search-buildings.md) | GET | Finds matching buildings in Infoplus. |
| [Update Building](actions/update-building.md) | PUT | Updates an existing building in Infoplus. |

### Carton

| Action | Method | Description |
| --- | --- | --- |
| [Create Carton](actions/create-carton.md) | POST | Creates a new carton in Infoplus. |
| [Delete Carton](actions/delete-carton.md) | DELETE | Deletes an existing carton from Infoplus. |
| [Search Cartons](actions/search-cartons.md) | GET | Finds matching cartons in Infoplus. |
| [Update Carton](actions/update-carton.md) | PUT | Updates an existing carton in Infoplus. |

### Carton Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Carton Activity](actions/create-carton-activity.md) | POST | Creates a new carton activity in Infoplus. |
| [Delete Carton Activity](actions/delete-carton-activity.md) | DELETE | Deletes an existing carton activity from Infoplus. |
| [Search Carton Activities](actions/search-carton-activities.md) | GET | Finds matching carton activities in Infoplus. |
| [Update Carton Activity](actions/update-carton-activity.md) | PUT | Updates an existing carton activity in Infoplus. |

### Carton Content

| Action | Method | Description |
| --- | --- | --- |
| [Create Carton Content](actions/create-carton-content.md) | POST | Creates a new carton content in Infoplus. |
| [Delete Carton Content](actions/delete-carton-content.md) | DELETE | Deletes an existing carton content from Infoplus. |
| [Search Carton Contents](actions/search-carton-contents.md) | GET | Finds matching carton contents in Infoplus. |
| [Update Carton Content](actions/update-carton-content.md) | PUT | Updates an existing carton content in Infoplus. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Infoplus. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Infoplus. |
| [Search Customers](actions/search-customers.md) | GET | Finds matching customers in Infoplus. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Infoplus. |

### External Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create External Shipment](actions/create-external-shipment.md) | POST | Creates a new external shipment in Infoplus. |
| [Delete External Shipment](actions/delete-external-shipment.md) | DELETE | Deletes an existing external shipment from Infoplus. |
| [Search External Shipments](actions/search-external-shipments.md) | GET | Finds matching external shipments in Infoplus. |
| [Update External Shipment](actions/update-external-shipment.md) | PUT | Updates an existing external shipment in Infoplus. |

### Fulfillment Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Fulfillment Plan](actions/create-fulfillment-plan.md) | POST | Creates a new fulfillment plan in Infoplus. |
| [Delete Fulfillment Plan](actions/delete-fulfillment-plan.md) | DELETE | Deletes an existing fulfillment plan from Infoplus. |
| [Search Fulfillment Plans](actions/search-fulfillment-plans.md) | GET | Finds matching fulfillment plans in Infoplus. |
| [Update Fulfillment Plan](actions/update-fulfillment-plan.md) | PUT | Updates an existing fulfillment plan in Infoplus. |

### Fulfillment Process

| Action | Method | Description |
| --- | --- | --- |
| [Search Fulfillment Processes](actions/search-fulfillment-processes.md) | GET | Finds matching fulfillment processes in Infoplus. |

### Inventory Adjustment

| Action | Method | Description |
| --- | --- | --- |
| [Search Inventory Adjustments](actions/search-inventory-adjustments.md) | GET | Finds matching inventory adjustments in Infoplus. |

### Inventory Detail

| Action | Method | Description |
| --- | --- | --- |
| [Search Inventory Details](actions/search-inventory-details.md) | GET | Finds matching inventory details in Infoplus. |

### Inventory Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Search Inventory Snapshots](actions/search-inventory-snapshots.md) | GET | Finds matching inventory snapshots in Infoplus. |

### Inventory Storage Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Inventory Storage Activity](actions/create-inventory-storage-activity.md) | POST | Creates a new inventory storage activity in Infoplus. |
| [Delete Inventory Storage Activity](actions/delete-inventory-storage-activity.md) | DELETE | Deletes an existing inventory storage activity from Infoplus. |
| [Search Inventory Storage Activities](actions/search-inventory-storage-activities.md) | GET | Finds matching inventory storage activities in Infoplus. |
| [Update Inventory Storage Activity](actions/update-inventory-storage-activity.md) | PUT | Updates an existing inventory storage activity in Infoplus. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in Infoplus. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from Infoplus. |
| [Search Items](actions/search-items.md) | GET | Finds matching items in Infoplus. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Infoplus. |

### Item Activity

| Action | Method | Description |
| --- | --- | --- |
| [Search Item Activities](actions/search-item-activities.md) | GET | Finds matching item activities in Infoplus. |

### Item Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Search Item Receipts](actions/search-item-receipts.md) | GET | Finds matching item receipts in Infoplus. |
| [Update Item Receipt](actions/update-item-receipt.md) | PUT | Updates an existing item receipt in Infoplus. |

### Item Receipt Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Item Receipt Activity](actions/create-item-receipt-activity.md) | POST | Creates a new item receipt activity in Infoplus. |
| [Delete Item Receipt Activity](actions/delete-item-receipt-activity.md) | DELETE | Deletes an existing item receipt activity from Infoplus. |
| [Search Item Receipt Activities](actions/search-item-receipt-activities.md) | GET | Finds matching item receipt activities in Infoplus. |
| [Update Item Receipt Activity](actions/update-item-receipt-activity.md) | PUT | Updates an existing item receipt activity in Infoplus. |

### Kit

| Action | Method | Description |
| --- | --- | --- |
| [Create Kit](actions/create-kit.md) | POST | Creates a new kit in Infoplus. |
| [Delete Kit](actions/delete-kit.md) | DELETE | Deletes an existing kit from Infoplus. |
| [Search Kits](actions/search-kits.md) | GET | Finds matching kits in Infoplus. |
| [Update Kit](actions/update-kit.md) | PUT | Updates an existing kit in Infoplus. |

### Line Of Business

| Action | Method | Description |
| --- | --- | --- |
| [Create Line of Business](actions/create-line-of-business.md) | POST | Creates a new line of business in Infoplus. |
| [Search Lines of Business](actions/search-lines-of-business.md) | GET | Finds matching lines of business in Infoplus. |
| [Update Line of Business](actions/update-line-of-business.md) | PUT | Updates an existing line of business in Infoplus. |

### Load

| Action | Method | Description |
| --- | --- | --- |
| [Search Loads](actions/search-loads.md) | GET | Finds matching loads in Infoplus. |

### Load Content

| Action | Method | Description |
| --- | --- | --- |
| [Search Load Contents](actions/search-load-contents.md) | GET | Finds matching load contents in Infoplus. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in Infoplus. |
| [Delete Location](actions/delete-location.md) | DELETE | Deletes an existing location from Infoplus. |
| [Search Locations](actions/search-locations.md) | GET | Finds matching locations in Infoplus. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Infoplus. |

### Location Footprint

| Action | Method | Description |
| --- | --- | --- |
| [Create Location Footprint](actions/create-location-footprint.md) | POST | Creates a new location footprint in Infoplus. |
| [Delete Location Footprint](actions/delete-location-footprint.md) | DELETE | Deletes an existing location footprint from Infoplus. |
| [Search Location Footprints](actions/search-location-footprints.md) | GET | Finds matching location footprints in Infoplus. |
| [Update Location Footprint](actions/update-location-footprint.md) | PUT | Updates an existing location footprint in Infoplus. |

### Low Stock

| Action | Method | Description |
| --- | --- | --- |
| [Search Low Stock Records](actions/search-low-stock-records.md) | GET | Finds matching low stock records in Infoplus. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Infoplus. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from Infoplus. |
| [Search Orders](actions/search-orders.md) | GET | Finds matching orders in Infoplus. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Infoplus. |

### Order Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Activity](actions/create-order-activity.md) | POST | Creates a new order activity in Infoplus. |
| [Delete Order Activity](actions/delete-order-activity.md) | DELETE | Deletes an existing order activity from Infoplus. |
| [Search Order Activities](actions/search-order-activities.md) | GET | Finds matching order activities in Infoplus. |
| [Update Order Activity](actions/update-order-activity.md) | PUT | Updates an existing order activity in Infoplus. |

### Order Line

| Action | Method | Description |
| --- | --- | --- |
| [Search Order Lines](actions/search-order-lines.md) | GET | Finds matching order lines in Infoplus. |

### Order Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Source](actions/create-order-source.md) | POST | Creates a new order source in Infoplus. |
| [Delete Order Source](actions/delete-order-source.md) | DELETE | Deletes an existing order source from Infoplus. |
| [Search Order Sources](actions/search-order-sources.md) | GET | Finds matching order sources in Infoplus. |
| [Update Order Source](actions/update-order-source.md) | PUT | Updates an existing order source in Infoplus. |

### Parcel Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Delete Parcel Invoice](actions/delete-parcel-invoice.md) | DELETE | Deletes an existing parcel invoice from Infoplus. |
| [Search Parcel Invoices](actions/search-parcel-invoices.md) | GET | Finds matching parcel invoices in Infoplus. |

### Receiving Process

| Action | Method | Description |
| --- | --- | --- |
| [Search Receiving Processes](actions/search-receiving-processes.md) | GET | Finds matching receiving processes in Infoplus. |

### Receiving Worksheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Receiving Worksheet](actions/create-receiving-worksheet.md) | POST | Creates a new receiving worksheet in Infoplus. |
| [Delete Receiving Worksheet](actions/delete-receiving-worksheet.md) | DELETE | Deletes an existing receiving worksheet from Infoplus. |
| [Search Receiving Worksheets](actions/search-receiving-worksheets.md) | GET | Finds matching receiving worksheets in Infoplus. |
| [Update Receiving Worksheet](actions/update-receiving-worksheet.md) | PUT | Updates an existing receiving worksheet in Infoplus. |

### Replenishment

| Action | Method | Description |
| --- | --- | --- |
| [Search Replenishments](actions/search-replenishments.md) | GET | Finds matching replenishments in Infoplus. |

### Replenishment Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Replenishment Plan](actions/create-replenishment-plan.md) | POST | Creates a new replenishment plan in Infoplus. |
| [Delete Replenishment Plan](actions/delete-replenishment-plan.md) | DELETE | Deletes an existing replenishment plan from Infoplus. |
| [Search Replenishment Plans](actions/search-replenishment-plans.md) | GET | Finds matching replenishment plans in Infoplus. |
| [Update Replenishment Plan](actions/update-replenishment-plan.md) | PUT | Updates an existing replenishment plan in Infoplus. |

### Return Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Search Return Shipments](actions/search-return-shipments.md) | GET | Finds matching return shipments in Infoplus. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Search Shipments](actions/search-shipments.md) | GET | Finds matching shipments in Infoplus. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST | Creates a new vendor in Infoplus. |
| [Delete Vendor](actions/delete-vendor.md) | DELETE | Deletes an existing vendor from Infoplus. |
| [Search Vendors](actions/search-vendors.md) | GET | Finds matching vendors in Infoplus. |
| [Update Vendor](actions/update-vendor.md) | PUT | Updates an existing vendor in Infoplus. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Create Warehouse](actions/create-warehouse.md) | POST | Creates a new warehouse in Infoplus. |
| [Search Warehouses](actions/search-warehouses.md) | GET | Finds matching warehouses in Infoplus. |
| [Update Warehouse](actions/update-warehouse.md) | PUT | Updates an existing warehouse in Infoplus. |

### Zone

| Action | Method | Description |
| --- | --- | --- |
| [Create Zone](actions/create-zone.md) | POST | Creates a new zone in Infoplus. |
| [Delete Zone](actions/delete-zone.md) | DELETE | Deletes an existing zone from Infoplus. |
| [Search Zones](actions/search-zones.md) | GET | Finds matching zones in Infoplus. |
| [Update Zone](actions/update-zone.md) | PUT | Updates an existing zone in Infoplus. |

