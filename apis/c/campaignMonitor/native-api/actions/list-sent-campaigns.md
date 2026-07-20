# List Sent Campaigns with Campaign Monitor

Retrieves sent campaigns for a Campaign Monitor client.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:clientId/campaigns.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Sent Campaigns](https://www.campaignmonitor.com/api/v3-3/clients/#getting-sent-campaigns-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | Campaign Monitor client identifier. |
