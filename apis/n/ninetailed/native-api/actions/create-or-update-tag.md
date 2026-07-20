# Create Or Update Tag with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/tags/:tagId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Or Update Tag](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/tags/tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `tagId` | path | `string` | yes | Contentful tag ID. Must be unique within the environment. |
| `name` | body | `string` | yes | Tag display name. Must be unique within the environment. |
