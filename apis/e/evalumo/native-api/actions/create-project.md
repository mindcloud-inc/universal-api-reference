# Create Project with Evalumo

Creates a new project in Evalumo.

## Endpoint

- **Method:** `POST`
- **Path:** `/project`
- **Base URL:** `https://api.evalumo.com`
- **Official documentation:** [Create Project](https://evalumo.apidocumentation.com/reference#tag/project/POST/project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_name` | body | `string` | yes | Construction project name. |
| `client_name` | body | `string` | no | Client or company name for the project. |
| `client_email` | body | `string` | no | Client email address. |
| `client_phone` | body | `string` | no | Client phone number. |
| `client_address` | body | `string` | no | Client street address. |
