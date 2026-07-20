# Fetch Prospects Events with Explorium

Fetches prospect events from Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/events`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Fetch Prospects Events](https://developers.explorium.ai/reference/prospects/events/fetch_prospects_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_types[]` | body | `array<string>` | yes | The prospect event types to fetch. |
| `prospect_ids[]` | body | `array<string>` | yes | The Explorium prospect identifiers to query. |
