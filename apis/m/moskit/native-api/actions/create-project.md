# Create Project with Moskit

Creates a new project in Moskit.

## Endpoint

- **Method:** `POST`
- **Path:** `projects`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Create Project](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `createdBy.id` | body | `number` | yes |
| `responsible.id` | body | `number` | yes |
| `step.id` | body | `number` | yes |
| `archived` | body | `boolean` | yes |
| `previsionCloseDate` | body | `date` | no |
