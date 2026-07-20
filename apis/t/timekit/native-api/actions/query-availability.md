# Query Availability with Timekit

Finds available booking timeslots in Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/availability`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Query Availability](https://developers.timekit.io/reference/query-availability-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buffer` | body | `string` | no | Buffer time around existing events. |
| `constraints[]` | body | `array<object>` | no | Availability constraint objects. |
| `from` | body | `string` | no | Beginning of the search space. |
| `length` | body | `string` | no | Length of each available time slot. |
| `mode` | body | `list<string>` | yes | Availability mode. Accepted values: `exclusive`, `mutual`, `roundrobin_prioritized`, `roundrobin_random`. |
| `output_timezone` | body | `string` | no | Timezone for returned time slots. |
| `project_id` | body | `string` | no | Project ID to derive availability settings from. |
| `resources[]` | body | `array<string>` | no | Resource IDs to include in the availability search. |
| `round_to_nearest_hour` | body | `boolean` | no | Round timeslots to the nearest hour. |
| `timeslot_increments` | body | `string` | no | Increments used for time slot starts. |
| `to` | body | `string` | no | End of the search space. |
