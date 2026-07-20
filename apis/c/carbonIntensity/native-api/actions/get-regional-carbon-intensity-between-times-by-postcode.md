# Get Regional Carbon Intensity Between Times By Postcode with Carbon Intensity

Retrieves regional carbon intensity between datetimes by postcode.

## Endpoint

- **Method:** `GET`
- **Path:** `/regional/intensity/:from/:to/postcode/:postcode`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Regional Carbon Intensity Between Times By Postcode](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
| `to` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
| `postcode` | path | `string` | yes | Valid outward postcode such as SW1A, EH1, M1, or BS1. |
