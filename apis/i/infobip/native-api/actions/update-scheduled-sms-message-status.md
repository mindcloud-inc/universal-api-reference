# Update Scheduled SMS Message Status with Infobip

## Endpoint

- **Method:** `PUT`
- **Path:** `/sms/1/bulks/status`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Update Scheduled SMS Message Status](https://www.infobip.com/docs/api/channels/sms/outbound-sms/update-scheduled-sms-messages-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkId` | query | `string` | yes | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. |
| `status` | body | `string` | yes | The status of the message(s). |
