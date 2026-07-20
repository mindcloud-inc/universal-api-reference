# Update Project with 4HSE

Updates an existing project in 4HSE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/project/update/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Update Project](https://docs.4hse.com/en/api/project/#operation-updateProject-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The project_id to update. |
| `name` | body | `string` | yes | The company name. Maximum length: 50. |
| `country` | body | `string` | yes | ISO 3166-1 alpha-2 country code. Maximum length: 2. |
| `description` | body | `string` | no | Optional free-text description. |
| `project_type` | body | `string` | no | Project type. |
| `status` | body | `string` | no | Project lifecycle status. |
