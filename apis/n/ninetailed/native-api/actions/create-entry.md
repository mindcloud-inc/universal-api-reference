# Create Entry with Ninetailed

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:space_id/environments/:environment_id/entries`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Entry](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entries-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
| `contentTypeId` | body | `string` | yes | Content type ID to send as the X-Contentful-Content-Type header. |
| `fields` | body | `object` | yes | Localized entry fields object. |
