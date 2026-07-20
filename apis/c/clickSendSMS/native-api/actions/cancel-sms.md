# Cancel SMS with ClickSend SMS

Cancels an SMS message in ClickSend SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/sms/:message_id/cancel`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Cancel SMS](https://developers.clicksend.com/docs/messaging/sms/other/cancel-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | Outbound message identifier to cancel. |
