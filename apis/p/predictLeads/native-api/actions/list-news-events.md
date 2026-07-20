# List News Events with PredictLeads

Retrieves news events from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/news_events`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List News Events](https://docs.predictleads.com/api_endpoints/news_events_dataset/retrieve_news_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories` | query | `string` | no | Comma-separated news event categories. |
| `company_location` | query | `string` | no | Filter news events by company location. |
