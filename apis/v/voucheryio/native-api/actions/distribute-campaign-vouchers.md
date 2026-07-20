# Distribute Campaign Vouchers with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign_id/vouchers/distribute`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Distribute Campaign Vouchers](https://docs.vouchery.io/reference/getapiv21campaignscampaignidvouchersdistribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | query | `number` | no | Number of vouchers to distribute |
| `campaign_id` | path | `number` | yes | Campaign ID |
