# List Subscribers by Location with HotspotSystem

Retrieves subscribers at a specific location from HotspotSystem.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:locationId/subscribers`
- **Base URL:** `https://api.hotspotsystem.com/v2.0`
- **Official documentation:** [List Subscribers by Location](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getsubscribersbylocationid)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | The ID of a location. |
| `fields` | query | `string` | no | Comma-separated list of response properties to include. |
