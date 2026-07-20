# Update Campaign with Vouchery.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:campaign_id`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Update Campaign](https://docs.vouchery.io/reference/putapiv21campaignscampaignid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Vouchery. |
| `currency` | body | `string` | yes | Alpha-3 currency code. |
| `description` | body | `string` | no | Updated campaign description. |
| `name` | body | `string` | no | Updated campaign name. |
| `status` | body | `string` | no | Updated campaign status. |
| `team` | body | `string` | no | Updated campaign team. |
| `type` | body | `string` | yes | Campaign type discriminator for update. |
