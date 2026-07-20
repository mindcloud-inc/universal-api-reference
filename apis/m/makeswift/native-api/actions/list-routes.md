# List Routes with Makeswift

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/routes`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [List Routes](https://docs.makeswift.com/developer/reference/api/routes/list-routes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | The site ID to list routes from. |
| `limit` | query | `number` | no | Maximum number of routes to return (1-100). |
| `startingAfter` | query | `string` | no | Pagination cursor ID. |
