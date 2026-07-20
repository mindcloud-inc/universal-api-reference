# Get Inbound SMS with ClickSend SMS

Retrieves an inbound SMS message from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms/inbound/:original_message_id`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Get Inbound SMS](https://developers.clicksend.com/docs/messaging/sms/other/view-a-specific-inbound-sms-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `original_message_id` | path | `string` | yes | Original inbound message identifier. |
