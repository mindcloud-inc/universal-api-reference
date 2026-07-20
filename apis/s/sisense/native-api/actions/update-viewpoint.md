# Update Viewpoint with Sisense

Updates an existing viewpoint in Sisense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/infusion/viewpoints/:id`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Update Viewpoint](https://developer.sisense.com/guides/restApi/infusion-api.html#put-infusion-viewpoints-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated viewpoint description. |
| `id` | path | `string` | no | The Viewpoint identifier. |
| `name` | body | `string` | no | The updated viewpoint name. |
