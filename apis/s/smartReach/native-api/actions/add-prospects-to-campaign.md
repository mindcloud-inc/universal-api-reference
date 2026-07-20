# Add Prospects To Campaign with SmartReach

Adds prospects to a campaign in SmartReach.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaign_id/prospects`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Add Prospects To Campaign](https://help.smartreach.io/reference/post_campaigns-campaign-id-prospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of campaign to return |
| `prospect_ids[]` | body | `array<string>` | yes | Prospect IDs to add to the campaign. |
| `ignore_prospects_in_other_campaigns` | body | `string` | no | How to handle prospects already present in other campaigns. |
