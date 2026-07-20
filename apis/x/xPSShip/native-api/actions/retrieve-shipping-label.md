# Retrieve Shipping Label with XPS Ship

Retrieves a shipping label from XPS Ship.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v1/customers/:customerId/shipments/:bookNumber/label/:labelImageFormat`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Retrieve Shipping Label](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/retrieve-shipping-label/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookNumber` | path | `string` | yes | XPS Ship shipment book number. |
| `labelImageFormat` | path | `string` | yes | Requested label format, PDF or PNG. |
