# Search Restrooms with Refuge Restrooms

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/restrooms/search`
- **Base URL:** `https://www.refugerestrooms.org/api`
- **Official documentation:** [Search Restrooms](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1RestroomsSearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Full-text search query for restroom records. |
| `ada` | query | `boolean` | no | Only return restrooms that are ADA accessible. |
| `unisex` | query | `boolean` | no | Only return restrooms that are unisex. |
| `offset` | query | `number` | no | Pad a number of results. |
