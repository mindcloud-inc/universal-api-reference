# List Space Pages with GitBook

Retrieves pages from a GitBook space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/content/pages`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Space Pages](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `computed` | query | `boolean` | no |
| `metadata` | query | `boolean` | no |
| `spaceId` | path | `string` | yes |
