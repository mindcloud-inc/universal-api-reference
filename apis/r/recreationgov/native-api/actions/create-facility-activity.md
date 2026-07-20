# Create Facility Activity with Recreation.gov

Creates a facility activity in Recreation.gov.

## Endpoint

- **Method:** `POST`
- **Path:** `/facilities/{id}/activities`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Create Facility Activity](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `number` | yes |
| `id` | path | `number` | yes |
| `description` | body | `string` | no |
| `feeDescription` | body | `string` | no |
