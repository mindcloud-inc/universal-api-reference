# Update Job Activity with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/jobactivity/:uuid.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Update Job Activity](https://developer.servicem8.com/reference/updatejobactivities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uuid` | path | `string` | yes |
| `job_uuid` | body | `string` | no |
| `staff_uuid` | body | `string` | no |
| `start_date` | body | `date` | no |
| `end_date` | body | `date` | no |
| `activity_was_scheduled` | body | `boolean` | no |
| `activity_was_recorded` | body | `boolean` | no |
| `material_uuid` | body | `string` | no |
| `activity_was_automated` | body | `string` | no |
| `has_been_opened` | body | `boolean` | no |
| `has_been_opened_timestamp` | body | `date` | no |
| `travel_time_in_seconds` | body | `number` | no |
| `travel_distance_in_meters` | body | `number` | no |
