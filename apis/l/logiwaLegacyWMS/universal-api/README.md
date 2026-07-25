# <img src="https://images.mindcloud.co/apps/icons/logiwa-legacy-wms-icon_1782393874174.png" alt="Logiwa Legacy WMS logo" width="28" height="28"> Logiwa Legacy WMS: Universal API

Logiwa Legacy WMS through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logiwaLegacyWMS/latest
- **Category:** Commerce
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://developer.logiwa.com/?id=5df0da39e6466c2eec992f3f

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pack Types (SEARCH)](actions/get-pack-type-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-pack-type-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory](actions/list-inventory.md) | GET |  |
| [List Inventory Stock Levels](actions/list-inventory-stock-levels.md) | GET | By using this endpoint, the users can obtain their current inventories based on the locations and also they may obtain some attributes such… |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get a Product ID](actions/get-a-product-id.md) | POST |  |
| [List Pack Types (SEARCH)](actions/get-pack-type-info.md) | GET | By using these endpoints, the users can obtain all the information that is related to the pack types of the items. To obtain this… |
| [List Pack Types (GET)](actions/list-pack-types-get.md) | GET | By using these endpoints, the users can obtain all the information that is related to the pack types of the items. To obtain this… |
| [List Shipment Info - Import](actions/list-shipment-info-import.md) | POST |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |
| [Update Receipt Order Detail](actions/update-receipt-order-detail.md) | POST | By using this endpoint, users can UPDATE the details of receipt orders if the ID field exists in the endpoint request. Users can CREATE… |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Insert Purchase Order](actions/insert-purchase-order.md) | POST | By using this endpoint, the users can create single or multiple purchase orders with lines. All the products used should be defined in the… |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | By using this endpoint, the users can obtain the list of all the purchase orders based on the entered criteria. |

### Receipt Order

| Action | Method | Description |
| --- | --- | --- |
| [Insert Receipt Order](actions/insert-receipt-order.md) | POST |  |
| [List Receipt Orders](actions/list-receipt-orders.md) | GET |  |

### Return Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Receipt Report](actions/get-receipt-report.md) | POST | By using this endpoint, the users can obtain the receipt records. |

### Shipment Order

| Action | Method | Description |
| --- | --- | --- |
| [Insert Shipment Order](actions/insert-shipment-order.md) | POST |  |
| [List Shipment Orders](actions/list-shipment-orders.md) | GET |  |

