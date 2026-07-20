# Get Regional Carbon Intensity Previous 24 Hours with Carbon Intensity

Retrieves 24-hour regional carbon intensity before a datetime.

## Endpoint

- **Method:** `GET`
- **Path:** `/regional/intensity/:from/pt24h`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Regional Carbon Intensity Previous 24 Hours](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
