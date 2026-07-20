# Get Flight with Schiphol Airport

Retrieves a flight from Schiphol Airport by flight ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/flights/:id`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [Get Flight](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights-id/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique numeric Schiphol flight ID. |
