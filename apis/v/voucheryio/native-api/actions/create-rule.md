# Create Rule with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaign_id/rules`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Rule](https://docs.vouchery.io/reference/postapiv21campaignscampaignidrules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from the path. |
| `type` | body | `string` | yes | Rule type. |
| `operator` | body | `string` | yes | Comparison operator for rule types that use it. |
| `value` | body | `number` | yes | Value for rule types that use it. |
