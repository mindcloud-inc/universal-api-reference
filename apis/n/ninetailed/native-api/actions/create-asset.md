# Create Asset with Ninetailed

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:space_id/environments/:environment_id/assets`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Asset](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/assets-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
| `fields` | body | `object` | yes | Localized asset fields object, including title and file metadata. |
