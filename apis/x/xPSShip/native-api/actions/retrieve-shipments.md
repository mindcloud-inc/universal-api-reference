# Retrieve Shipments with XPS Ship

Retrieves shipments from XPS Ship.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v1/customers/:customerId/shipments`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Retrieve Shipments](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/retrieve-shipments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minBookNumber` | query | `string` | yes | Minimum shipment book number for listing shipments. |
