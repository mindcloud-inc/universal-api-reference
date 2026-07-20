# Update Webhook with CampaignKit

Updates an existing webhook subscription in CampaignKit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/webhooks/{{id}}`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Update Webhook](https://campaignkit.cc/docs/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the webhook subscription is active. |
| `events[]` | body | `array<string>` | no | Updated webhook event subscriptions. Accepted values: `0`, `1`. |
| `id` | path | `number` | yes | Webhook ID. |
| `url` | body | `string` | no | Updated destination URL for the webhook. |
