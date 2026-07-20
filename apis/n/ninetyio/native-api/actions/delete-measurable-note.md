# Delete Measurable Note with Ninety.io

Deletes a measurable note from Ninety.io for a period.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/scorecard/kpis/:kpiId/notes/:periodStartDate`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Delete Measurable Note](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `kpiId` | path | `string` | yes |
| `periodStartDate` | path | `date` | yes |
