# Update facility activity with Atlar

Updates an existing facility activity in Atlar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/financial-data/v2beta/facilities/{id}/activities/{activityId}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Update facility activity](https://docs.atlar.com/reference/patch-financial-data-v2beta-facilities-id-activities-activityid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `activityId` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
