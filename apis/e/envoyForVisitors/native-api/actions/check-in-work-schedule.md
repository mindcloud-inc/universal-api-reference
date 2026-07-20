# Check In Work Schedule with Envoy for Visitors

Checks in a work schedule in Envoy for Visitors.

## Endpoint

- **Method:** `POST`
- **Path:** `/work-schedules/:id/checkin`
- **Base URL:** `https://api.envoy.com/v1`
- **Official documentation:** [Check In Work Schedule](https://developers.envoy.com/hub/reference/checkinworkschedule)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
