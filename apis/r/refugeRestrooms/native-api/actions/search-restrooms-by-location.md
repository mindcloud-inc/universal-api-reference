# Search Restrooms by Location with Refuge Restrooms

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/restrooms/by_location`
- **Base URL:** `https://www.refugerestrooms.org/api`
- **Official documentation:** [Search Restrooms by Location](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1RestroomsByLocation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude to search around. |
| `lng` | query | `number` | yes | Longitude to search around. |
| `ada` | query | `boolean` | no | Only return restrooms that are ADA accessible. |
| `unisex` | query | `boolean` | no | Only return restrooms that are unisex. |
| `offset` | query | `number` | no | Pad a number of results. |
