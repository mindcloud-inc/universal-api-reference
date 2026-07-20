# List Social Transactions by Location with HotspotSystem

Retrieves social transactions at a specific location from HotspotSystem.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:locationId/transactions/social`
- **Base URL:** `https://api.hotspotsystem.com/v2.0`
- **Official documentation:** [List Social Transactions by Location](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getsocialtransactionsbylocationid)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | The ID of a location. |
| `fields` | query | `string` | no | Comma-separated list of response properties to include. |
