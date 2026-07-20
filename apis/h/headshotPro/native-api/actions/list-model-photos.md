# List Model Photos with HeadshotPro

Retrieves photos for a model in HeadshotPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/models/:modelId/photos`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [List Model Photos](https://www.headshotpro.com/api/photos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | ID of the model whose photos should be listed. |
| `status` | query | `string` | no | Optional photo status filter. |
| `likedStatus` | query | `string` | no | Optional rating filter: none, liked, or loved. |
| `include` | query | `string` | no | URL variants to include: main or all. |
