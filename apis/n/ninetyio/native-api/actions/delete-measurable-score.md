# Delete Measurable Score with Ninety.io

Deletes a measurable score from Ninety.io for a period.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/scorecard/kpis/:kpiId/scores/:periodStartDate`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Delete Measurable Score](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `kpiId` | path | `string` | yes |
| `periodStartDate` | path | `date` | yes |
