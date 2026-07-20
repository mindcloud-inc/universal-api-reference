# List Event Occurrences with Ticket Tailor

Retrieves event occurrences for a Ticket Tailor event series.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/event_series/:event_series_id/events`
- **Base URL:** `https://api.tickettailor.com`
- **Official documentation:** [List Event Occurrences](https://developers.tickettailor.com/docs/api/get-all-event-occurrences/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_series_id` | path | `string` | yes | Ticket Tailor event series ID. |
