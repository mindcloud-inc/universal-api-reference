# Create Project with 4HSE

Creates a new project in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/project/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Project](https://docs.4hse.com/en/api/project/#operation-createProject-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The company name. Maximum length: 50. |
| `country` | body | `string` | yes | ISO 3166-1 alpha-2 country code. Maximum length: 2. |
| `description` | body | `string` | no | Optional free-text description. |
| `project_type` | body | `string` | no | Project type. |
| `status` | body | `string` | no | Project lifecycle status. |
