# Create Voucher with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaign_id/vouchers`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Voucher](https://docs.vouchery.io/reference/postapiv21campaignscampaignidvouchers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from the path. |
| `code` | body | `string` | yes | Voucher code to create. |
| `customer_identifier` | body | `string` | no | Optional customer identifier to assign the voucher. |
| `gift_card_value` | body | `number` | no | Optional gift card value for gift card vouchers. |
| `activates_at` | body | `string` | no | Optional activation timestamp. |
| `voucher_valid_until` | body | `string` | no | Optional voucher expiration timestamp. |
