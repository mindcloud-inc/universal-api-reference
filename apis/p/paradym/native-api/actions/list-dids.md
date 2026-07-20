# List DIDs with Paradym

Retrieves a list of DIDs from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/dids`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List DIDs](https://paradym.id/reference#tag/dids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search[did]` | query | `string` | no | Search DIDs by DID value. |
| `filter[method]` | query | `string` | no | Filter DIDs by DID method. |
| `filter[network]` | query | `string` | no | Filter DIDs by network. |
