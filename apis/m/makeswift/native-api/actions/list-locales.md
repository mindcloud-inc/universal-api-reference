# List Locales with Makeswift

Retrieves locales for a site from Makeswift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/locales`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [List Locales](https://docs.makeswift.com/developer/reference/api/locales/list-locales)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | The site ID to list locales from. |
| `limit` | query | `number` | no | Maximum number of locales to return (1-100). |
| `startingAfter` | query | `string` | no | Pagination cursor ID. |
