# Retrieve Shipment with XPS Ship

Retrieves a shipment from XPS Ship.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v1/customers/:customerId/shipments/:bookNumber`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Retrieve Shipment](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/retrieve-shipment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookNumber` | path | `string` | yes | XPS Ship shipment book number. |
