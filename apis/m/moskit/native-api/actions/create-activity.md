# Create Activity with Moskit

Creates a new activity in Moskit.

## Endpoint

- **Method:** `POST`
- **Path:** `activities`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Create Activity](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `createdBy.id` | body | `number` | yes |
| `responsible.id` | body | `number` | yes |
| `dueDate` | body | `date` | yes |
| `type.id` | body | `number` | yes |
| `duration` | body | `number` | no |
| `notes` | body | `string` | no |
