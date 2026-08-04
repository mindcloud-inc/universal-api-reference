# List Service Areas with Toast

Retrieves service areas configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/serviceAreas`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Service Areas](https://doc.toasttab.com/openapi/configuration/operation/serviceAreasGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
