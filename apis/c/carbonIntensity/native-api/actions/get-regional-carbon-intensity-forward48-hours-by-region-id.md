# Get Regional Carbon Intensity Forward 48 Hours By Region ID with Carbon Intensity

Retrieves 48-hour regional carbon intensity after a datetime by region.

## Endpoint

- **Method:** `GET`
- **Path:** `/regional/intensity/:from/fw48h/regionid/:regionid`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Regional Carbon Intensity Forward 48 Hours By Region ID](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
| `regionid` | path | `number` | yes | Region ID defined by the Carbon Intensity API. |
