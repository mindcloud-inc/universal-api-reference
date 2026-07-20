# Activate Content Type with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:space_id/environments/:environment_id/content_types/:content_type_id/published`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Activate Content Type](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type-activation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
| `content_type_id` | path | `string` | yes | Contentful content type ID. |
| `contentfulVersion` | body | `number` | yes | Current content type version to send as X-Contentful-Version. |
