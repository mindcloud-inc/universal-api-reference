# Create KPI with Weekdone

Creates a new KPI in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `kpi`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Create KPI](https://weekdone.com/developer#h-kpis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `decimals` | body | `number` | no |
| `department_id` | body | `number` | no |
| `description` | body | `string` | yes |
| `maxval` | body | `number` | no |
| `startval` | body | `number` | no |
| `team_id` | body | `number` | no |
| `type` | body | `string` | yes |
