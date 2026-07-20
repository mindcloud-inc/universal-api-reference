# Vehicle Market Value with Vincario

## Endpoint

- **Method:** `GET`
- **Path:** `/:apiKey/:controlSum/vehicle-market-value/:vin.:format`
- **Base URL:** `https://api.vincario.com/3.2`
- **Official documentation:** [Vehicle Market Value](https://vincario.com/api-docs/3.2/#operations-Vehicle_Market_Value-Vehicle_Market_Value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vin` | path | `string` | yes | Vehicle Identification Number. |
| `odometer` | query | `number` | no | Optional odometer reading used for price-adjusted calculations. |
| `odometer_unit` | query | `string` | no | Optional odometer unit. Supported values are km or mi. |
