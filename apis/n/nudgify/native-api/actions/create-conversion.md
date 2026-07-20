# Create Conversion with Nudgify

Creates conversion events in Nudgify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/conversions`
- **Base URL:** `https://app.nudgify.com`
- **Official documentation:** [Create Conversion](https://www.nudgify.com/docs/knowledge-base/rest-api-for-sign-ups/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversions[]` | body | `array<object>` | yes | One or more conversion events to send to Nudgify. |
| `conversions[].date` | body | `string` | yes | UTC timestamp in `Y-m-d H:i:s` format. |
| `conversions[].email` | body | `string` | no | Email address tied to the conversion. |
| `conversions[].first_name` | body | `string` | no | First name to show in the nudge. |
| `conversions[].last_name` | body | `string` | no | Last name to show in the nudge. |
| `conversions[].ip` | body | `string` | no | IP address used for location fallback. |
| `conversions[].city` | body | `string` | no | City to show in the nudge. |
| `conversions[].state` | body | `string` | no | State or region to show in the nudge. |
| `conversions[].country` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
