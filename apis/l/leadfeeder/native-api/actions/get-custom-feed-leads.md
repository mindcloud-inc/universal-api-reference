# Get Leads For Custom Feed with Leadfeeder

Retrieves leads for a custom feed in Leadfeeder by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/custom-feeds/:customFeedId/leads`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Get Leads For Custom Feed](https://docs.leadfeeder.com/api/#get-leads-for-custom-feed)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFeedId` | path | `string` | yes |
| `start_date` | query | `date` | yes |
| `end_date` | query | `date` | yes |
