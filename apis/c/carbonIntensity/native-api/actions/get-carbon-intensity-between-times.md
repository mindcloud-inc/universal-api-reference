# Get Carbon Intensity Between Times with Carbon Intensity

Retrieves carbon intensity between two specified datetimes.

## Endpoint

- **Method:** `GET`
- **Path:** `/intensity/:from/:to`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Carbon Intensity Between Times](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
| `to` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
