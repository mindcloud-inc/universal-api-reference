# Create or Update Measurable Score with Ninety.io

Creates or updates a measurable score in Ninety.io for a period.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scorecard/kpis/:kpiId/scores`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Create or Update Measurable Score](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `kpiId` | path | `string` | yes |
| `value` | body | `number` | yes |
| `periodStartDate` | body | `date` | yes |
