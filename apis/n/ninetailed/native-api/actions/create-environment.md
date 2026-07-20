# Create Environment with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:space_id/environments/:environment_id`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Environment](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments/environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Environment ID to create. Contentful limits environment IDs to 40 characters. |
| `name` | body | `string` | yes | Human-readable environment name. |
