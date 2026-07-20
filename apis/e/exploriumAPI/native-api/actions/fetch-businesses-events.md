# Fetch Businesses Events with Explorium

Fetches business events from Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/events`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Fetch Businesses Events](https://developers.explorium.ai/reference/businesses/events/fetch_businesses_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_ids[]` | body | `array<string>` | yes | The Explorium business identifiers to query. |
| `event_types[]` | body | `array<string>` | yes | The business event types to fetch. |
