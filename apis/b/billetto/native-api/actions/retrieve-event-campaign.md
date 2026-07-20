# Retrieve Event Campaign with Billetto

Retrieves an event campaign from Billetto.

## Endpoint

- **Method:** `GET`
- **Path:** `organiser/events/{id}/campaigns/{campaign_id}`
- **Base URL:** `https://billetto.dk/api/v3`
- **Official documentation:** [Retrieve Event Campaign](https://api.billetto.com/reference/retrieve-a-campaign-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Billetto event ID. |
| `campaign_id` | path | `string` | yes | Billetto campaign ID. |
