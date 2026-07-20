# Reschedule SMS Messages with Infobip

## Endpoint

- **Method:** `PUT`
- **Path:** `/sms/1/bulks`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Reschedule SMS Messages](https://www.infobip.com/docs/api/channels/sms/outbound-sms/reschedule-sms-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkId` | query | `string` | yes | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. |
| `sendAt` | body | `date` | yes | Date and time when the message is to be sent. Used for scheduled SMS (see [Scheduled SMS endpoints](#channels/sms/get-scheduled-sms-messages) for more details). Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`, and can only be scheduled for no later than 180 days in advance. |
