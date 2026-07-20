# List Tags with Ninetailed

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/environments/:environmentId/tags`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [List Tags](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/tags/tag-collection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
