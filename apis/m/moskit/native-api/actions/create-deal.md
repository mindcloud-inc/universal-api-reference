# Create Deal with Moskit

Creates a new deal in Moskit.

## Endpoint

- **Method:** `POST`
- **Path:** `deals`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Create Deal](https://moskit.stoplight.io/docs/api-v2/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `createdBy.id` | body | `number` | yes |
| `responsible.id` | body | `number` | yes |
| `status` | body | `string` | yes |
| `stage.id` | body | `number` | yes |
| `previsionCloseDate` | body | `date` | no |
| `price` | body | `number` | no |
| `closeDate` | body | `date` | no |
| `lostReason.id` | body | `number` | no |
