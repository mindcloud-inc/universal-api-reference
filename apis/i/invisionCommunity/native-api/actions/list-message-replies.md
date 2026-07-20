# List Message Replies with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/core/messages/:id/replies`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [List Message Replies](https://invisioncommunity.com/developers/rest-api/index/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Message identifier. |
