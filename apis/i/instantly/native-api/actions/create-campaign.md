# Create Campaign with Instantly

Creates a new campaign in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/campaigns`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Create Campaign](https://developer.instantly.ai/api/v2/campaign/createcampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the campaign. |
| `campaign_schedule` | body | `object` | yes | Campaign schedule object. |
| `sequences[]` | body | `array<object>` | no | Campaign email sequence array. |
