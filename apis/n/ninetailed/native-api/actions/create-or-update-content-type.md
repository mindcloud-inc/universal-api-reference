# Create Or Update Content Type with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:space_id/environments/:environment_id/content_types/:content_type_id`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Or Update Content Type](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
| `content_type_id` | path | `string` | yes | Contentful content type ID. |
| `name` | body | `string` | yes | Content type display name. |
| `fields[]` | body | `array<object>` | yes | Content type fields array. |
