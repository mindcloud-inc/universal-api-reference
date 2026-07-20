# Process Asset with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/assets/:assetId/files/:locale/process`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Process Asset](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-processing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `assetId` | path | `string` | yes | Asset ID to process. |
| `locale` | path | `string` | yes | Locale code for the asset file, such as en-US. |
