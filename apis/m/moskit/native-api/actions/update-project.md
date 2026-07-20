# Update Project with Moskit

Updates an existing project in Moskit.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:id`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Update Project](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
| `createdBy.id` | body | `number` | yes |
| `responsible.id` | body | `number` | yes |
| `step.id` | body | `number` | yes |
| `archived` | body | `boolean` | yes |
| `previsionCloseDate` | body | `date` | no |
