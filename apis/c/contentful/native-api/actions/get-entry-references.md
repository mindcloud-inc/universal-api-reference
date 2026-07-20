# Get entry references with Contentful

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/environments/:environmentId/entries/:entryId/references`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Get entry references](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entryId` | path | `string` | no |
| `environmentId` | path | `string` | no |
| `include` | query | `string` | no |
| `spaceId` | path | `string` | no |
