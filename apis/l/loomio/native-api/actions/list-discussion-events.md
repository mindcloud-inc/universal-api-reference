# List Discussion Events with Loomio

Retrieves discussion events from Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Discussion Events](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discussion_id` | query | `string` | no | The Loomio discussion ID to list events for. |
