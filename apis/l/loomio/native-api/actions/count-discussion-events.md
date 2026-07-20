# Count Discussion Events with Loomio

Counts discussion events in Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/count`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [Count Discussion Events](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discussion_id` | query | `string` | no | The Loomio discussion ID to count events for. |
