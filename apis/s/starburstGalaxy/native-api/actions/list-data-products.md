# List data products with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/dataProduct`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [List data products](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. |
| `pageToken` | query | `string` | no | Pagination token returned by a previous Starburst Galaxy API response. |
