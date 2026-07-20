# List Campaigns with Donorbox

Retrieves campaigns from Donorbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://donorbox.org/api/v1`
- **Official documentation:** [List Campaigns](https://github.com/donorbox/donorbox-api#campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter campaigns by exact campaign ID. |
