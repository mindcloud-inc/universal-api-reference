# Update SMS Campaign with ClickSend SMS

Updates an existing SMS campaign in ClickSend SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/sms-campaigns/:sms_campaign_id`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Update SMS Campaign](https://developers.clicksend.com/docs/messaging/sms-campaigns/other/view-sms-campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sms_campaign_id` | path | `number` | yes | ID of the SMS campaign to update. |
| `list_id` | body | `number` | yes | Target recipient list ID for the campaign. |
| `name` | body | `string` | yes | Campaign name. |
| `from` | body | `string` | yes | Sender name or number. |
| `body` | body | `string` | yes | SMS message content. |
| `schedule` | body | `number` | no | Unix timestamp for scheduled send. |
