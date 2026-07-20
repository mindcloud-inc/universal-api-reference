# List Campaign Redemptions with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign_id/redemptions`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [List Campaign Redemptions](https://docs.vouchery.io/reference/getapiv21campaignscampaignidredemptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID |
| `page` | query | `number` | no | Result page (indexed from 1) |
| `per_page` | query | `number` | no | Results per page |
