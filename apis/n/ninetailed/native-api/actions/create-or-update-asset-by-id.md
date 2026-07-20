# Create Or Update Asset By ID with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/assets/:assetId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Or Update Asset By ID](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `assetId` | path | `string` | yes | ID to assign to the asset or update. |
| `fields.title.en-US` | body | `string` | yes | Localized asset title for en-US. |
