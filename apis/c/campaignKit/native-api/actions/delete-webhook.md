# Delete Webhook with CampaignKit

Deletes an existing webhook subscription from CampaignKit.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/webhooks/{{id}}`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Delete Webhook](https://campaignkit.cc/docs/api/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Webhook ID. |
