# Create Time Off with Float

Creates a new time off entry in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/timeoffs`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Time Off](https://developer.float.com/api_reference.html#Time_Off)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeoff_type_id` | body | `number` | yes | The ID of this time off type |
| `start_date` | body | `string` | yes | Start date of this time off |
| `end_date` | body | `string` | yes | End date of this time off |
| `hours` | body | `number` | no | Number of hours per day for this time off |
| `timeoff_notes` | body | `string` | no | Additional notes about the time off |
| `repeat_state` | body | `number` | no | Frequency that this time off repeats |
| `status` | body | `number` | no | Status of the time off |
| `repeat_end` | body | `string` | no | Date that the repeating time off will cease |
| `full_day` | body | `number` | no | Whether this time off is for a full day |
| `people_ids` | body | `list<number>` | yes | List of people IDs assigned to this time off |
