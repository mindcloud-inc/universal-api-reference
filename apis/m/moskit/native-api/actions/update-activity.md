# Update Activity with Moskit

Updates an existing activity in Moskit.

## Endpoint

- **Method:** `PUT`
- **Path:** `activities/:id`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Update Activity](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `title` | body | `string` | yes |
| `createdBy.id` | body | `number` | yes |
| `responsible.id` | body | `number` | yes |
| `dueDate` | body | `date` | yes |
| `type.id` | body | `number` | yes |
| `duration` | body | `number` | no |
| `notes` | body | `string` | no |
| `doneDate` | body | `date` | no |
| `doneNotes` | body | `string` | no |
