# Create Campaign Reward with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaign_id/rewards`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Campaign Reward](https://docs.vouchery.io/reference/postapiv21campaignscampaignidrewards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from the path. |
| `type` | body | `string` | yes | Reward type. |
| `title` | body | `string` | yes | Reward title. |
| `description` | body | `string` | yes | Reward description. |
| `value` | body | `number` | yes | Reward value. |
