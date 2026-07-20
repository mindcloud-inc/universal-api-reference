# Update Facility Activity with Recreation.gov

Updates a facility activity in Recreation.gov.

## Endpoint

- **Method:** `PUT`
- **Path:** `/facilities/{id}/activities/{activityId}`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Update Facility Activity](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `number` | no |
| `id` | path | `number` | yes |
| `activityId` | path | `number` | yes |
| `description` | body | `string` | no |
| `feeDescription` | body | `string` | no |
