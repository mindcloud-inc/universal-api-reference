# Search Restrooms by Date with Refuge Restrooms

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/restrooms/by_date`
- **Base URL:** `https://www.refugerestrooms.org/api`
- **Official documentation:** [Search Restrooms by Date](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1RestroomsByDate)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `day` | query | `number` | yes | Day of the date filter. |
| `month` | query | `number` | yes | Month of the date filter. |
| `year` | query | `number` | yes | Year of the date filter. |
| `updated` | query | `boolean` | no | Return records updated, rather than created, since the given date. |
| `ada` | query | `boolean` | no | Only return restrooms that are ADA accessible. |
| `unisex` | query | `boolean` | no | Only return restrooms that are unisex. |
| `offset` | query | `number` | no | Pad a number of results. |
