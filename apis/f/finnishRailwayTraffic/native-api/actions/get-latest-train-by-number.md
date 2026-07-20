# Get latest train by number with Finnish Railway Traffic

Retrieves the latest train by number from Finnish Railway Traffic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/trains/latest/:train_number`
- **Base URL:** `https://rata.digitraffic.fi`
- **Official documentation:** [Get latest train by number](https://rata.digitraffic.fi/swagger/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `train_number` | path | `number` | yes | Train number, for example 1. |
