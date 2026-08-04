# List Discounts with Toast

Retrieves discounts configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/discounts`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Discounts](https://doc.toasttab.com/openapi/configuration/operation/discountsGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
