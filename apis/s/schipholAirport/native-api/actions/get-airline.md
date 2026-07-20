# Get Airline with Schiphol Airport

Retrieves an airline from Schiphol Airport by IATA or ICAO code.

## Endpoint

- **Method:** `GET`
- **Path:** `/airlines/:airline`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [Get Airline](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airline` | path | `string` | yes | IATA or ICAO airline code, such as KL or KLM. |
