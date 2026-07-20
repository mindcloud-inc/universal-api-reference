# List Topic Posts with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/forums/topics/:id/posts`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [List Topic Posts](https://invisioncommunity.com/developers/rest-api/index/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The topic identifier. |
