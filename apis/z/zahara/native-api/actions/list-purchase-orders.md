# List Purchase Orders with Zahara

Retrieves purchase orders from a Zahara business unit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/PurchaseOrder/Get/{{skip}}/{{take}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [List Purchase Orders](https://ask.zaharasoftware.com/api-docs/get-all-purchase-orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `skip` | path | `number` | yes | Number of records to skip. |
| `take` | path | `number` | yes | Number of records to return. |
