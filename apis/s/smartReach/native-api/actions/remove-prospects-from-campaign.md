# Remove Prospects From Campaign with SmartReach

Removes prospects from a campaign in SmartReach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:campaign_id/prospects`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Remove Prospects From Campaign](https://help.smartreach.io/reference/put_campaigns-campaign-id-prospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of campaign to return |
| `prospect_ids[]` | body | `array<string>` | yes | Prospect IDs to remove from the campaign. |
