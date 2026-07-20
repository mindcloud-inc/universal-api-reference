# Delete Content Type with Ninetailed

## Endpoint

- **Method:** `DELETE`
- **Path:** `/spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Delete Content Type](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `contentTypeId` | path | `string` | yes | Content type ID to delete. The content type must be deactivated first in Contentful. |
