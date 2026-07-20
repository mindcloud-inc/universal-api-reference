# Get Carbon Intensity Forward 24 Hours with Carbon Intensity

Retrieves carbon intensity for 24 hours after a datetime.

## Endpoint

- **Method:** `GET`
- **Path:** `/intensity/:from/fw24h`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Carbon Intensity Forward 24 Hours](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
