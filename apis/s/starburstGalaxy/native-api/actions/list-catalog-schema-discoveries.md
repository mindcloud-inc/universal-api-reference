# List catalog schema discoveries with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/catalog/{catalogId}/schemaDiscovery`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [List catalog schema discoveries](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `catalogId` | path | `string` | yes | Starburst Galaxy catalog ID. Docs also support URL-encoded lookup expressions such as name=value. |
| `latest` | query | `boolean` | no | Whether to return only the latest catalog schema discovery result. |
| `pageSize` | query | `number` | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. |
| `pageToken` | query | `string` | no | Pagination token returned by a previous Starburst Galaxy API response. |
