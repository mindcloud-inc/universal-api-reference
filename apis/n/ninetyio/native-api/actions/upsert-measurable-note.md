# Create or Update Measurable Note with Ninety.io

Creates or updates a measurable note in Ninety.io for a period.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scorecard/kpis/:kpiId/notes`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Create or Update Measurable Note](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `kpiId` | path | `string` | yes |
| `note` | body | `string` | yes |
| `periodStartDate` | body | `date` | yes |
