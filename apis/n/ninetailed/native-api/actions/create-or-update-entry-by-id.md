# Create Or Update Entry By ID with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:space_id/environments/:environment_id/entries/:entry_id`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Or Update Entry By ID](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
| `entry_id` | path | `string` | yes | Contentful entry ID. |
| `contentTypeId` | body | `string` | yes | Content type ID to send as X-Contentful-Content-Type when creating by ID. |
| `contentfulVersion` | body | `number` | no | Current entry version to send as X-Contentful-Version when updating an existing entry. |
| `fields` | body | `object` | yes | Localized entry fields object. |
