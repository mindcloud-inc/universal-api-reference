# Archive Asset with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/assets/:assetId/archived`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Archive Asset](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-archiving)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `assetId` | path | `string` | yes | Asset ID to archive. |
| `version` | body | `number` | yes | Current Contentful asset version for X-Contentful-Version. |
