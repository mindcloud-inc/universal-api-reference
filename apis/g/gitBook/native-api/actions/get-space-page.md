# Get Space Page with GitBook

Retrieves a page from a GitBook space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/content/page/:pageId`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Get Space Page](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `computed` | query | `boolean` | no |
| `format` | query | `string` | no |
| `metadata` | query | `boolean` | no |
| `pageId` | path | `string` | yes |
| `spaceId` | path | `string` | yes |
