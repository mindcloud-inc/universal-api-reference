# Create Project Without Consumption with Sunwise

Creates a new project without consumption data in Sunwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/create-project-without-consumption/`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Create Project Without Consumption](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | body | `string` | yes |
| `project_name` | body | `string` | yes |
| `zip_code` | body | `string` | no |
| `service_number` | body | `string` | no |
