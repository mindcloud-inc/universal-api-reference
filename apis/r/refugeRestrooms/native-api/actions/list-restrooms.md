# List Restrooms with Refuge Restrooms

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/restrooms`
- **Base URL:** `https://www.refugerestrooms.org/api`
- **Official documentation:** [List Restrooms](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1Restrooms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ada` | query | `boolean` | no | Only return restrooms that are ADA accessible. |
| `unisex` | query | `boolean` | no | Only return restrooms that are unisex. |
| `offset` | query | `number` | no | Pad a number of results. |
