# Get Leads with Leadfeeder

Retrieves leads for an account in Leadfeeder by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/leads`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Get Leads](https://docs.leadfeeder.com/api/#get-leads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | query | `date` | yes |
| `end_date` | query | `date` | yes |
