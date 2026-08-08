# Create order with Fraser Direct

## Endpoint

- **Method:** `POST`
- **Path:** `/CreateOrder`
- **Base URL:** `{baseURL}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderNumber` | body | `string` | no | Order number. OrderNumber or PO must be provided. |
| `PO` | body | `string` | no | Purchase order number. OrderNumber or PO must be provided. |
| `STName` | body | `string` | yes | Required ship-to name. |
| `STAddress1` | body | `string` | yes | Required ship-to address line 1. |
| `STAddress2` | body | `string` | no | Optional ship-to address line 2. |
| `STCity` | body | `string` | yes | Required ship-to city. |
| `STProvince` | body | `string` | yes | Required 2-character ship-to province. |
| `STPostalCode` | body | `string` | yes | Required ship-to postal code. |
| `STCountry` | body | `string` | yes | Required 3-character country code. |
| `ShipPhone` | body | `string` | no | Optional ship-to phone number. |
| `PODate` | body | `string` | yes | Required order date in YYYY-MM-DD format. |
| `RequestedDeliveryDate` | body | `string` | no | Optional requested delivery date in YYYY-MM-DD format. |
| `WarehouseIntructions` | body | `string` | no | Optional warehouse instructions. Fraser Direct's field name is spelled WarehouseIntructions in the API docs. |
| `Carrier` | body | `string` | no | Optional carrier. If omitted, Fraser Direct rate shops based on ServiceLevel. |
| `ServiceLevel` | body | `string` | yes | Required service level. Valid values are STANDARD or EXPRESS. |
| `DetailList` | body | `object<object>` | no | — |
| `ReferenceNumber` | body | `string` | no | — |
