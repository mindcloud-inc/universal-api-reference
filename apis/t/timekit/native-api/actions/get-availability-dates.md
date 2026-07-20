# Get Availability Dates with Timekit

Retrieves available booking dates from Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/availability/dates`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Get Availability Dates](https://developers.timekit.io/reference/availabilitydates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Beginning of the search space. |
| `project_id` | body | `string` | no | Project ID to derive availability settings from. |
| `resources[]` | body | `array<string>` | no | Resource IDs to include in the availability search. |
| `to` | body | `string` | no | End of the search space. |
