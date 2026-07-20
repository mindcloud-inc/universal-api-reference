# List Airlines with Schiphol Airport

Retrieves a list of airlines from Schiphol Airport.

## Endpoint

- **Method:** `GET`
- **Path:** `/airlines`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [List Airlines](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights/get)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Result page number, starting at 0. |
| `sort` | query | `string` | no | Sort expression using publicName, iata, icao, or nvls. |
