# Get Delivery Order Status with Dachser

Retrieves delivery order status from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/deliveryorderstatus`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Delivery Order Status](https://api-portal.dachser.com/bi.b2b.portal/api/library/deliveryorderstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchase-order-number` | query | `string` | no | Purchase order number. |
| `reference-number1` | query | `string` | no | First delivery order reference number. |
| `reference-number2` | query | `string` | no | Second delivery order reference number. |
| `reference-number3` | query | `string` | no | Third delivery order reference number. |
| `delivery-order-date` | query | `date` | no | Delivery order date. |
| `event-code` | query | `string` | no | Warehouse order status event code. |
| `customer-id` | query | `string` | no | Optional customer ID. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
