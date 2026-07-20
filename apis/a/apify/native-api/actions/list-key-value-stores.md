# List Key-Value Stores with Apify

Retrieves key-value stores from Apify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/key-value-stores`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Key-Value Stores](https://docs.apify.com/api/v2/key-value-stores-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownership` | query | `string` | no | Filter key-value stores by ownership: ownedByMe or sharedWithMe. |
