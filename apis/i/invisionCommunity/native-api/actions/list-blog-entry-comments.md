# List Blog Entry Comments with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/blog/entries/:id/comments`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [List Blog Entry Comments](https://invisioncommunity.com/developers/rest-api/index/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The blog entry identifier. |
