# Create Webhook with CampaignKit

Creates a new webhook subscription in CampaignKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Create Webhook](https://campaignkit.cc/docs/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Webhook event types to subscribe to. Accepted values: `0`, `1`. |
| `url` | body | `string` | yes | Destination URL that receives CampaignKit webhook events. |
