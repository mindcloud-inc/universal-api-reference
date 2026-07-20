# Auto-Assign Tasks with Onfleet

Assigns tasks to workers automatically in Onfleet.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/autoAssign`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Auto-Assign Tasks](https://docs.onfleet.com/reference/automatically-assign-list-of-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks[]` | body | `array<string>` | yes | An array of task IDs to assign. |
| `options.mode` | body | `string` | yes | The desired automatic assignment mode. Either distance or load. |
| `options.teams[]` | body | `array<string>` | no | An array of team IDs to consider for automatic assignment. |
| `options.maxAssignedTaskCount` | body | `number` | no | The maximum number of tasks a worker can have after automatic assignment. |
| `options.considerDependencies` | body | `boolean` | no | Whether to include dependency families in the assignment operation. |
| `options.excludedWorkerIds[]` | body | `array<string>` | no | One or more worker IDs that should not be considered in assignment calculations. |
| `options.restrictAutoAssignmentToTeam` | body | `boolean` | no | Whether to restrict auto-assignment strictly to the provided teams. |
