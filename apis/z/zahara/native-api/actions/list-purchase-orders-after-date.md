# List Purchase Orders After Date with Zahara

Retrieves purchase orders from Zahara after a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/PurchaseOrder/After/{{date}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [List Purchase Orders After Date](https://ask.zaharasoftware.com/api-docs/get-orders-after-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Return purchase orders updated after this date. |
