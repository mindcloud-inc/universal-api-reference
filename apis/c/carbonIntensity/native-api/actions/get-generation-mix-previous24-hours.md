# Get Generation Mix Previous 24 Hours with Carbon Intensity

Retrieves generation mix for 24 hours before a datetime.

## Endpoint

- **Method:** `GET`
- **Path:** `/generation/:from/pt24h`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Generation Mix Previous 24 Hours](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
