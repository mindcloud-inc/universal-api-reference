# Get Event Occurrence with Ticket Tailor

Retrieves an event occurrence from Ticket Tailor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/event_series/:event_series_id/events/:event_occurrence_id`
- **Base URL:** `https://api.tickettailor.com`
- **Official documentation:** [Get Event Occurrence](https://developers.tickettailor.com/docs/api/get-event-occurrence-by-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_series_id` | path | `string` | yes | Ticket Tailor event series ID. |
| `event_occurrence_id` | path | `string` | yes | Ticket Tailor event occurrence ID. |
