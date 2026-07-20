# List Flight IDs with Schiphol Airport

Retrieves flight IDs from Schiphol Airport by datetime range.

## Endpoint

- **Method:** `GET`
- **Path:** `/flights/ids`
- **Base URL:** `https://api.schiphol.nl/public-flights`
- **Official documentation:** [List Flight IDs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights-id/get)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDateTime` | query | `string` | yes | Start of the scheduleDateTime range, formatted yyyy-MM-ddTHH:mm:ss. |
| `toDateTime` | query | `string` | yes | End of the scheduleDateTime range, formatted yyyy-MM-ddTHH:mm:ss. Maximum range is three days. |
