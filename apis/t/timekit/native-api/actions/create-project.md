# Create Project with Timekit

Creates a new project in Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Create Project](https://developers.timekit.io/reference/projects-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allow_conference` | body | `string` | no |
| `availability` | body | `object` | yes |
| `availability_constraints[]` | body | `array<object>` | no |
| `booking` | body | `object` | yes |
| `customer_fields` | body | `object` | no |
| `meta` | body | `object` | no |
| `name` | body | `string` | yes |
| `reminders[]` | body | `array<object>` | no |
| `resources[]` | body | `array<string>` | yes |
| `slug` | body | `string` | no |
| `ui` | body | `object` | no |
