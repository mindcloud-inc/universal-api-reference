# Update Deal with Moskit

Updates an existing deal in Moskit.

## Endpoint

- **Method:** `PUT`
- **Path:** `deals/:id`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Update Deal](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
| `createdBy.id` | body | `number` | yes |
| `responsible.id` | body | `number` | yes |
| `status` | body | `string` | yes |
| `stage.id` | body | `number` | yes |
| `previsionCloseDate` | body | `date` | no |
| `price` | body | `number` | no |
| `closeDate` | body | `date` | no |
| `lostReason.id` | body | `number` | no |
