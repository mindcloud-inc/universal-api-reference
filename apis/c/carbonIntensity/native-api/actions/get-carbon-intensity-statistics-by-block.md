# Get Carbon Intensity Statistics By Block with Carbon Intensity

Retrieves block-based carbon intensity statistics between two datetimes.

## Endpoint

- **Method:** `GET`
- **Path:** `/intensity/stats/:from/:to/:block`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Carbon Intensity Statistics By Block](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
| `to` | path | `string` | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. |
| `block` | path | `string` | yes | Aggregation block. Verified runtime example: 24h. |
