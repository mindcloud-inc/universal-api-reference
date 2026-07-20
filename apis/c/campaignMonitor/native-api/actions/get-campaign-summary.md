# Get Campaign Summary with Campaign Monitor

Retrieves summary metrics for a sent Campaign Monitor campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/summary.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Get Campaign Summary](https://www.campaignmonitor.com/api/v3-3/campaigns/#campaign-summary-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign Monitor campaign identifier. |
