# List Aircraft Types with Schiphol Airport

Retrieves aircraft types from Schiphol Airport.

## Endpoint

- **Method:** `GET`
- **Path:** `/aircrafttypes`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [List Aircraft Types](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/aircrafttypes/get)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iataMain` | query | `string` | no | Three-character IATA main aircraft type code. |
| `iataSub` | query | `string` | no | Three-character IATA sub aircraft type code. |
| `page` | query | `number` | no | Result page number, starting at 0. |
| `sort` | query | `string` | no | Sort expression using iataMain, iataSub, longDescription, or shortDescription. |
