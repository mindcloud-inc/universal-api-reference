# Get Property Listings with Alto

Retrieves property listings from Alto by property IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/listing/property/items`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Property Listings](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property-id` | query | `string` | no | Property listing identifier to retrieve. Send multiple values as a string separated by `,`. |
