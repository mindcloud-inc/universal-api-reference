# Update Project with Insightful

Updates an existing project in your Insightful account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project/:id`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Update Project](https://developers.insightful.io/#4a5f4df0-97cb-438e-af9f-9a762235c524)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | body | `boolean` | no | Whether the project is archived. |
| `description` | body | `string` | no | The updated project description. |
| `employees[]` | body | `array<string>` | no | Employee IDs assigned to the project. |
| `id` | path | `string` | yes | The project ID to update. |
| `name` | body | `string` | no | The updated project name. |
| `screenshotSettings` | body | `object` | no | Screenshot settings for the project. |
