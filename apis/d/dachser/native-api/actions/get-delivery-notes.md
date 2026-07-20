# Get Delivery Notes with Dachser

Retrieves delivery notes from Dachser by reference or date.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/deliverynotes`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Delivery Notes](https://api-portal.dachser.com/bi.b2b.portal/api/library/deliverynotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchase-order-number` | query | `string` | no | Purchase order number. |
| `reference-number1` | query | `string` | no | First delivery note reference number. |
| `reference-number2` | query | `string` | no | Second delivery note reference number. |
| `reference-number3` | query | `string` | no | Third delivery note reference number. |
| `delivery-order-date` | query | `date` | no | Delivery order date. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
