# Get Collection with Underdog Protocol

Retrieves a collection from Underdog Protocol.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/collections/:collectionAddress`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Get Collection](https://docs.underdogprotocol.com/resources/v1/collections/retrieve-a-collection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `collectionAddress` | path | `string` | yes |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
