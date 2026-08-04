# List Dining Options with Toast

Retrieves dining options configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/diningOptions`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Dining Options](https://doc.toasttab.com/openapi/configuration/operation/diningOptionsGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
