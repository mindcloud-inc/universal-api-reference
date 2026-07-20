# Add a target rule to a ramp schedule with GrowthBook

Adds a target rule to a GrowthBook ramp schedule.

## Endpoint

- **Method:** `POST`
- **Path:** `/ramp-schedules/:id/actions/add-target`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Add a target rule to a ramp schedule](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `featureId` | body | `string` | yes |
| `ruleId` | body | `string` | yes |
| `environment` | body | `string` | yes |
