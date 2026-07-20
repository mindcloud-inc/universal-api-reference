# Remove a target rule from a ramp schedule with GrowthBook

Removes a target rule from a GrowthBook ramp schedule.

## Endpoint

- **Method:** `POST`
- **Path:** `/ramp-schedules/:id/actions/eject-target`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Remove a target rule from a ramp schedule](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `targetId` | body | `string` | no | Target ID (from the targets array) |
| `ruleId` | body | `string` | no | Rule ID — use with environment as an alternative to targetId |
| `environment` | body | `string` | no | Environment — use with ruleId as an alternative to targetId |
