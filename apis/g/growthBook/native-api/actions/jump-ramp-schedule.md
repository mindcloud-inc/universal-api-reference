# Jump to a specific step with GrowthBook

Jumps to a specific step in a GrowthBook ramp schedule.

## Endpoint

- **Method:** `POST`
- **Path:** `/ramp-schedules/:id/actions/jump`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Jump to a specific step](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `targetStepIndex` | body | `number` | yes | Zero-based index of the step to jump to; -1 = pre-start |
