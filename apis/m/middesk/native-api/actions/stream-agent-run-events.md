# Stream agent run events with Middesk

Retrieves streamed events for a Middesk agent run.

## Endpoint

- **Method:** `GET`
- **Path:** `/runs/:id/stream`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Stream agent run events](https://docs.middesk.com/reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the agent run whose event stream you want to read. |
