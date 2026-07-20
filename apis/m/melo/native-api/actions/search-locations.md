# Search Locations with Melo

Finds locations in Melo by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/location-autocomplete`
- **Base URL:** `https://preprod-api.notif.immo`
- **Official documentation:** [Search Locations](https://docs.melo.io/api-reference/endpoint/indicators/locations)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text for location suggestions. |
