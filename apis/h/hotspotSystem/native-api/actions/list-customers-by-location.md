# List Customers by Location with HotspotSystem

Retrieves customers at a specific location from HotspotSystem.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:locationId/customers`
- **Base URL:** `https://api.hotspotsystem.com/v2.0`
- **Official documentation:** [List Customers by Location](https://www.hotspotsystem.com/apidocs/api/reference/#operation-getcustomersbylocationid)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | The ID of a location. |
| `fields` | query | `string` | no | Comma-separated list of response properties to include. |
