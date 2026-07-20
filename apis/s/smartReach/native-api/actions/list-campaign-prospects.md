# List Campaign Prospects with SmartReach

Retrieves campaign prospects from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign_id/prospects`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Campaign Prospects](https://help.smartreach.io/reference/get_campaigns-campaign-id-prospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of campaign to return |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
