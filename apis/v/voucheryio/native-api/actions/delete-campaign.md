# Delete Campaign with Vouchery.io

## Endpoint

- **Method:** `DELETE`
- **Path:** `/campaigns/:campaign_id`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Delete Campaign](https://docs.vouchery.io/reference/deleteapiv21campaignscampaignid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Vouchery. |
| `force` | query | `boolean` | no | Force deletion when Vouchery reports dependent vouchers or redemptions. |
