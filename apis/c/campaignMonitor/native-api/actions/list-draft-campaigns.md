# List Draft Campaigns with Campaign Monitor

Retrieves draft campaigns for a Campaign Monitor client.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:clientId/drafts.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Draft Campaigns](https://www.campaignmonitor.com/api/v3-3/clients/#getting-draft-campaigns-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | Campaign Monitor client identifier. |
