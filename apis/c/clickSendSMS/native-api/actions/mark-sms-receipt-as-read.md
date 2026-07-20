# Mark SMS Receipt As Read with ClickSend SMS

Marks SMS receipts as read in ClickSend SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/sms/receipts-read`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Mark SMS Receipt As Read](https://developers.clicksend.com/docs/messaging/sms/other/mark-sms-receipt-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_before` | body | `string` | yes | Mark receipts as read before this timestamp/date. |
