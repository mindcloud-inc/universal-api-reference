# Filter Listings with Alto

Finds property listings in Alto by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/listing/filter`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Filter Listings](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch-id` | query | `string` | no | Branch identifier filter. |
| `owner-id` | query | `string` | no | Owner contact identifier filter. |
| `status` | query | `string` | no | Listing status filter. |
