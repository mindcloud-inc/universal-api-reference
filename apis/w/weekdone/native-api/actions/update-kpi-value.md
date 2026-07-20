# Update KPI Value with Weekdone

Updates progress for a KPI in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `kpi/:kpiId/progress`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update KPI Value](https://weekdone.com/developer#h-kpis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `kpiId` | path | `number` | yes |
| `value` | body | `number` | yes |
