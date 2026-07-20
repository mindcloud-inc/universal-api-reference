# Get Availability Counts with Timekit

Retrieves available timeslot counts from Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/availability/count`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Get Availability Counts](https://developers.timekit.io/reference/availabilitycount)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `buffer` | body | `string` | no |
| `from` | body | `string` | no |
| `length` | body | `string` | no |
| `project_id` | body | `string` | no |
| `resources[]` | body | `array<string>` | no |
| `timeslot_increments` | body | `string` | no |
| `to` | body | `string` | no |
