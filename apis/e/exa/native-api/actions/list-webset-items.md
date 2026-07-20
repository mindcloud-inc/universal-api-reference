# List Webset Items with Exa

Retrieves webset items from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/websets/v0/websets/:webset/items`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [List Webset Items](https://exa.ai/docs/websets/api/websets/items/list-all-items-for-a-webset)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id or externalId of the Webset |
| `sourceId` | query | `string` | no | The id of the source |
