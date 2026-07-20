# Set Events Webhook URL with WotNot

Updates the events webhook URL in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:account_id/webhook`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Set Events Webhook URL](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `number` | yes |
| `webhook_url` | body | `string` | yes |
| `token` | body | `string` | yes |
| `is_enabled` | body | `boolean` | yes |
