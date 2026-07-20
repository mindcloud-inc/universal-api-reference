# Cancel SMS Campaign with ClickSend SMS

Cancels an existing SMS campaign in ClickSend SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/sms-campaigns/:sms_campaign_id/cancel`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Cancel SMS Campaign](https://developers.clicksend.com/docs/messaging/sms-campaigns/other/view-sms-campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sms_campaign_id` | path | `number` | yes | ID of the SMS campaign to cancel. |
