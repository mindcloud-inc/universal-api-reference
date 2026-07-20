# Update a single rampSchedule with GrowthBook

Updates an existing ramp schedule in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ramp-schedules/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single rampSchedule](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `steps[]` | body | `array<object>` | no |
| `endActions[]` | body | `array<object>` | no |
| `startDate` | body | `date` | no |
| `endCondition` | body | `object` | no |
