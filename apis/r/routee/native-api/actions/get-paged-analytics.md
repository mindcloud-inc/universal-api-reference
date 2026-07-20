# Get paged analytics with Routee

Retrieves paged analytics data from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/shorten/:trackingId/analytics`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get paged analytics](https://docs.routee.net/reference/getting-paged-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | — |
| `from` | query | `string` | yes | Start date for analytics report |
| `to` | query | `string` | yes | End date for analytics report |
| `page` | query | `string` | no | [Optional] Index for results (0 is first result) |
| `size` | query | `string` | no | [Optional]  Number of results per page (Default 20 max according to capability) |
| `link` | body | `string` | no | The shortened URL |
| `longUrl` | body | `string` | no | The original URL |
| `visits[]` | body | `array<object>` | no | The information for each click on the shortened URL. |
| `tags` | body | `string` | no | A map of string field values to store information |
