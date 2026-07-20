# Update KPI with Weekdone

Updates an existing KPI in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `kpi/:kpiId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update KPI](https://weekdone.com/developer#h-kpis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | yes |
| `kpiId` | path | `number` | yes |
