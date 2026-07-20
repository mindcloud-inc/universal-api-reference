# Create Project with Insightful

Creates a new project in your Insightful account.

## Endpoint

- **Method:** `POST`
- **Path:** `/project`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Create Project](https://developers.insightful.io/#4566c05a-bd50-459f-8f0c-e35975c44130)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `boolean` | no | Whether the project is billable. |
| `deadline` | body | `number` | no | Project deadline in milliseconds. |
| `description` | body | `string` | no | A description for the project. |
| `employees[]` | body | `array<string>` | yes | Employee IDs to assign to the project. |
| `name` | body | `string` | yes | The project name. |
| `payroll` | body | `object` | no | Payroll settings for the project. |
| `priorities[]` | body | `array<string>` | no | Possible project priorities. |
| `statuses[]` | body | `array<string>` | no | Possible project statuses. |
