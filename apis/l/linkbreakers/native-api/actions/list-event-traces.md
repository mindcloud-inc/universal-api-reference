# List Event Traces with Linkbreakers

Retrieves a list of event traces from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:eventId/traces`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [List Event Traces](https://linkbreakers.com/help/api/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The ID of the event to list traces for. |
