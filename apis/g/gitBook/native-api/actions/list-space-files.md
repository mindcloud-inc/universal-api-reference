# List Space Files with GitBook

Retrieves files from a GitBook space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/content/files`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Space Files](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `computed` | query | `boolean` | no |
| `metadata` | query | `boolean` | no |
| `spaceId` | path | `string` | yes |
