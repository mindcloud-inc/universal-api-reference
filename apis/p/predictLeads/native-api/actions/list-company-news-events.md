# List Company News Events with PredictLeads

Retrieves news events for a PredictLeads company.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/news_events`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company News Events](https://docs.predictleads.com/api_endpoints/news_events_dataset/retrieve_company_s_news_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company's ID or domain. |
| `categories` | query | `string` | no | Comma-separated news event categories. |
| `found_at_from` | query | `string` | no | Include news events found on or after this date. |
| `found_at_until` | query | `string` | no | Include news events found on or before this date. |
