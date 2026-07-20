# Get Unavailable Slots with Timekit

Retrieves unavailable booking timeslots from Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/unavailable/slots`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Get Unavailable Slots](https://developers.timekit.io/reference/unavailable-slots)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `buffer` | body | `string` | no |
| `from` | body | `string` | no |
| `length` | body | `string` | no |
| `output_timezone` | body | `string` | no |
| `project_id` | body | `string` | no |
| `resources[]` | body | `array<string>` | no |
| `timeslot_increments` | body | `string` | no |
| `to` | body | `string` | no |
