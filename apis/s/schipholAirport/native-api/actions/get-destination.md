# Get Destination with Schiphol Airport

Retrieves a destination from Schiphol Airport by IATA code.

## Endpoint

- **Method:** `GET`
- **Path:** `/destinations/:iata`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [Get Destination](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/destinations-iata/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iata` | path | `string` | yes | Three-character destination IATA code. |
