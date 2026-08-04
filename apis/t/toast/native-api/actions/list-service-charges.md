# List Service Charges with Toast

Retrieves service charges configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/serviceCharges`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Service Charges](https://doc.toasttab.com/openapi/configuration/operation/serviceChargesGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
