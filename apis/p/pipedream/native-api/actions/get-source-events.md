# Get source events with Pipedream

Retrieves event summaries for a source in Pipedream.

## Endpoint

- **Method:** `GET`
- **Path:** `/sources/{id}/event_summaries`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Get source events](https://pipedream.com/docs/rest-api/api-reference/events/get-source-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The source identifier. |
