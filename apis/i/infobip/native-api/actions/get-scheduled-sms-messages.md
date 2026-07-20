# Get Scheduled SMS Messages with Infobip

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/1/bulks`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Get Scheduled SMS Messages](https://www.infobip.com/docs/api/channels/sms/outbound-sms/get-scheduled-sms-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkId` | query | `string` | yes | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. |
