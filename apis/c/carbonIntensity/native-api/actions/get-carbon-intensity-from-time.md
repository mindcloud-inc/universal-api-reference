# Get Carbon Intensity From Time with Carbon Intensity

Retrieves carbon intensity from a specific datetime.

## Endpoint

- **Method:** `GET`
- **Path:** `/intensity/:from`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Carbon Intensity From Time](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
