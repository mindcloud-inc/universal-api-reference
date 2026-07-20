# List Events with Zulip

Retrieves events from a Zulip event queue.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [List Events](https://zulip.com/api/get-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_event_id` | query | `number` | no | The last event ID the client has successfully processed. |
| `queue_id` | query | `string` | yes | The event queue ID returned by Register Event Queue. |
