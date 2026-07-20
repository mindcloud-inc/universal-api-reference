# List Suppliers After Date with Zahara

Retrieves suppliers from Zahara after a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/Supplier/After/{{date}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [List Suppliers After Date](https://ask.zaharasoftware.com/api-docs/get-suppliers-after-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Return suppliers updated after this date. |
