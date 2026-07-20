# List clusters with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/cluster`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [List clusters](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extended` | query | `boolean` | no | Whether to include extended cluster details when supported by Starburst Galaxy. |
| `pageSize` | query | `number` | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. |
| `pageToken` | query | `string` | no | Pagination token returned by a previous Starburst Galaxy API response. |
