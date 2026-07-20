# Update Rec Area Activity with Recreation.gov

Updates a recreation area activity in Recreation.gov.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recareas/{id}/activities/{activityId}`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Update Rec Area Activity](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `number` | no |
| `id` | path | `number` | yes |
| `activityId` | path | `number` | yes |
| `description` | body | `string` | no |
| `feeDescription` | body | `string` | no |
