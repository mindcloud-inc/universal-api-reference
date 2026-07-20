# Create a single rampScheduleTemplate with GrowthBook

Creates a new ramp schedule template in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/ramp-schedule-templates`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single rampScheduleTemplate](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `steps[]` | body | `array<object>` | yes |
| `endPatch` | body | `object` | no |
| `official` | body | `boolean` | no |
