# Get Integration Events with Socket

Retrieves organization integration events from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/settings/integrations/:integration_id/events`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Get Integration Events](https://docs.socket.dev/reference/getintegrationevents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `integration_id` | path | `string` | yes |
