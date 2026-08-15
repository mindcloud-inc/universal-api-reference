# Get Vehicle Stats with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `fleet/vehicles/stats`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [Get Vehicle Stats](https://developers.samsara.com/reference/getvehiclestats)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `types[]` | query | `array<string>` | yes | Vehicle statistic types to return; up to three types. |
| `time` | query | `string` | no | Return the latest statistics at or before this RFC 3339 timestamp. |
