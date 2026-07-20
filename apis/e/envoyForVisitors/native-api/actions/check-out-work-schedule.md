# Check Out Work Schedule with Envoy for Visitors

Checks out a work schedule in Envoy for Visitors.

## Endpoint

- **Method:** `POST`
- **Path:** `/work-schedules/:id/checkout`
- **Base URL:** `https://api.envoy.com/v1`
- **Official documentation:** [Check Out Work Schedule](https://developers.envoy.com/hub/reference/checkoutworkschedule)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
