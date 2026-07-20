# Delete source events with Pipedream

Deletes all events for a source in Pipedream.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sources/{id}/events`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Delete source events](https://pipedream.com/docs/rest-api/api-reference/events/delete-source-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The source identifier. |
