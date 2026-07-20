# Mark Inbound SMS as Read with ClickSend SMS

Marks inbound SMS messages as read in ClickSend SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/sms/inbound-read`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Mark Inbound SMS as Read](https://developers.clicksend.com/docs/messaging/sms/other/mark-inbound-sms-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_before` | body | `string` | yes | Mark inbound SMS as read before this timestamp/date. |
