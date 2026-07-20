# List Season Episodes with Simplecast

Retrieves episodes for a season from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/seasons/:season_id/episodes`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Season Episodes](https://apidocs.simplecast.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `season_id` | path | `string` | yes | Simplecast season identifier. |
