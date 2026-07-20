# List Points of Interest with Melo

Retrieves points of interest from Melo near specific coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/indicators/points_of_interest`
- **Base URL:** `https://preprod-api.notif.immo`
- **Official documentation:** [List Points of Interest](https://docs.melo.io/api-reference/endpoint/indicators/points_of_interest)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude coordinate. |
| `lon` | query | `number` | yes | Longitude coordinate. |
| `radius` | query | `number` | no | Search radius in kilometers. |
| `facilities` | query | `string<string>` | yes | Facility types to include, comma-separated (for example school,kindergarten,bus_stop). |
