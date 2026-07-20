# Delete facility activity with Atlar

Deletes an existing facility activity from Atlar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/financial-data/v2beta/facilities/{id}/activities/{activityId}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Delete facility activity](https://docs.atlar.com/reference/delete-financial-data-v2beta-facilities-id-activities-activityid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `activityId` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
