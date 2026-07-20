# List Discussion Position Keys with Loomio

Retrieves discussion position keys from Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/position_keys`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Discussion Position Keys](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discussion_id` | query | `string` | no | The Loomio discussion ID to list position keys for. |
