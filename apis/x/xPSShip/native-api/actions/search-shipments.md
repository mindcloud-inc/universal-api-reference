# Search Shipments with XPS Ship

Finds booked shipments in XPS Ship by keyword.

## Endpoint

- **Method:** `POST`
- **Path:** `/restapi/v1/customers/:customerId/searchShipments`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Search Shipments](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/search-shipments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | yes | Shipment search keyword. |
