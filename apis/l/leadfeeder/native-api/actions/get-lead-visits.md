# Get Lead Visits with Leadfeeder

Retrieves visits for a lead in Leadfeeder by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/leads/:leadId/visits`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Get Lead Visits](https://docs.leadfeeder.com/api/#get-all-visits-of-a-lead)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leadId` | path | `string` | yes |
| `start_date` | query | `date` | yes |
| `end_date` | query | `date` | yes |
