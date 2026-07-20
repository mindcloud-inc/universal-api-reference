# Unpublish Asset with Ninetailed

## Endpoint

- **Method:** `DELETE`
- **Path:** `/spaces/:spaceId/environments/:environmentId/assets/:assetId/published`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Unpublish Asset](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-publishing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `assetId` | path | `string` | yes | Asset ID to unpublish. |
