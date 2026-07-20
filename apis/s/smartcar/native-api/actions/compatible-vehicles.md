# Compatible Vehicles with Smartcar

Retrieves compatible vehicles from Smartcar.

## Endpoint

- **Method:** `GET`
- **Path:** `https://compatibility.api.smartcar.com/v3/compatible-vehicles`
- **Base URL:** `https://vehicle.api.smartcar.com/v3`
- **API:** rest
- **Official documentation:** [Compatible Vehicles](https://smartcar.com/docs/api-reference/compatible-vehicles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[make]` | query | `string` | no | Filter compatible vehicles by vehicle make. |
| `filter[powertrainType]` | query | `string` | no | Filter compatible vehicles by powertrain type. |
| `filter[region]` | query | `string` | no | Filter compatible vehicles by region. |
