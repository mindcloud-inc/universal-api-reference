# Get SMS Receipt with ClickSend SMS

Retrieves an SMS receipt from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms/receipts/:message_id`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Get SMS Receipt](https://developers.clicksend.com/docs/messaging/sms/other/view-specific-sms-receipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | Message identifier returned by send/history/receipts endpoints. |
