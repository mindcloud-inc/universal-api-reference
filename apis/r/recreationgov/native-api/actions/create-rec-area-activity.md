# Create Rec Area Activity with Recreation.gov

Creates a recreation area activity in Recreation.gov.

## Endpoint

- **Method:** `POST`
- **Path:** `/recareas/{id}/activities`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Create Rec Area Activity](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `number` | yes |
| `id` | path | `number` | yes |
| `description` | body | `string` | no |
| `feeDescription` | body | `string` | no |
