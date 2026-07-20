# Publish Asset with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/assets/:assetId/published`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Publish Asset](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-publishing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `assetId` | path | `string` | yes | Asset ID to publish. |
| `version` | body | `number` | yes | Current Contentful asset version for X-Contentful-Version. |
