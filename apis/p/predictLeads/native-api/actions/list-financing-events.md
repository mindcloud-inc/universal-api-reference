# List Financing Events with PredictLeads

Retrieves financing events from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/financing_events`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Financing Events](https://docs.predictleads.com/api_endpoints/financing_events_dataset/retrieve_financing_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_location` | query | `string` | no | Filter financing events by company location. |
| `financing_types_normalized` | query | `string` | no | Comma-separated normalized financing event types. |
