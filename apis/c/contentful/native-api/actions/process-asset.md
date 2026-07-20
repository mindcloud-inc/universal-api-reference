# Process asset with Contentful

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/assets/:assetId/files/:localeCode/process`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Process asset](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assetId` | path | `string` | no |
| `environmentId` | path | `string` | no |
| `localeCode` | path | `string` | no |
| `spaceId` | path | `string` | no |
