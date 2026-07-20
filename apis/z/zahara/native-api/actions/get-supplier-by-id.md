# Get Supplier By ID with Zahara

Retrieves a supplier by ID from Zahara.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/Supplier/Get/{{supplierId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Get Supplier By ID](https://ask.zaharasoftware.com/api-docs/get-supplier-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `supplierId` | path | `number` | yes | The Zahara supplier ID. |
