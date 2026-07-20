# Get Campaign Statistics with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign_id/stats`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Get Campaign Statistics](https://docs.vouchery.io/reference/getapiv21campaignscampaignidstats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Vouchery. |
| `range` | query | `number` | no | Statistics range in days. Default 30, max 90. |
