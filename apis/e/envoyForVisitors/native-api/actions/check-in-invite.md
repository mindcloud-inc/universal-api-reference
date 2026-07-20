# Check In Invite with Envoy for Visitors

Checks in a visitor from an invite in Envoy for Visitors.

## Endpoint

- **Method:** `POST`
- **Path:** `/invites/:id/checkin`
- **Base URL:** `https://api.envoy.com/v1`
- **Official documentation:** [Check In Invite](https://developers.envoy.com/hub/reference/checkininvite)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
