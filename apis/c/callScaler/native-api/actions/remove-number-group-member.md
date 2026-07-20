# Remove Number Group Member with CallScaler

Deletes a number group member from CallScaler.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/number-groups/:id/members/:numId`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Remove Number Group Member](https://callscaler.com/docs/api-resources)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `numId` | path | `string` | yes |
