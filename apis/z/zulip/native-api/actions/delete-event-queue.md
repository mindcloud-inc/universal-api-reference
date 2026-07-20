# Delete Event Queue with Zulip

Deletes an existing Zulip event queue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/events`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Delete Event Queue](https://zulip.com/api/delete-queue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queue_id` | query | `string` | yes | The event queue ID returned by Register Event Queue. |
