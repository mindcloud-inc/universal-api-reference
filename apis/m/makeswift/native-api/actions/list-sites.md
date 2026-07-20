# List Sites with Makeswift

Retrieves sites from Makeswift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sites`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [List Sites](https://docs.makeswift.com/developer/reference/api/sites/list-sites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | yes | Workspace ID to list sites from. |
| `limit` | query | `number` | no | Maximum number of sites to return (1-100). |
| `startingAfter` | query | `string` | no | Cursor ID to continue pagination. |
