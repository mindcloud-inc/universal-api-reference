# List Request Queues with Apify

Retrieves request queues from Apify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/request-queues`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Request Queues](https://docs.apify.com/api/v2/request-queues-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownership` | query | `string` | no | Filter request queues by ownership: ownedByMe or sharedWithMe. |
