# Update a single rampScheduleTemplate with GrowthBook

Updates an existing ramp schedule template in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ramp-schedule-templates/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single rampScheduleTemplate](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `steps[]` | body | `array<object>` | no |
| `endPatch` | body | `object` | no |
| `official` | body | `boolean` | no |
