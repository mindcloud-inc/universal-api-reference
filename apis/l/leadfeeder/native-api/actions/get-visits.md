# Get Visits with Leadfeeder

Retrieves visits for an account in Leadfeeder by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/visits`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Get Visits](https://docs.leadfeeder.com/api/#get-all-visits)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | query | `date` | yes |
| `end_date` | query | `date` | yes |
