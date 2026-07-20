# Get Purchase Order By ID with Zahara

Retrieves a purchase order by ID from Zahara.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/PurchaseOrder/Get/{{documentId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Get Purchase Order By ID](https://ask.zaharasoftware.com/api-docs/get-purchase-order-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Purchase order document ID. |
