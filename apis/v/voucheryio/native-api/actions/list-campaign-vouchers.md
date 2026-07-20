# List Campaign Vouchers with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaign_id/vouchers`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [List Campaign Vouchers](https://docs.vouchery.io/reference/getapiv21campaignscampaignidvouchers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID |
| `code` | query | `string` | no | Voucher code |
| `created_by_task_id` | query | `string` | no | Queue task UUID |
| `page` | query | `number` | no | Result page (indexed from 1) |
| `per_page` | query | `number` | no | Results per page |
| `status` | query | `string` | no | Voucher status |
