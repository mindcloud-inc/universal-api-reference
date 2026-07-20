# Cancel Scheduled SMS Message with smsmode

## Endpoint

- **Method:** `DELETE`
- **Path:** `sms/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Cancel Scheduled SMS Message](https://dev.smsmode.com/sms/v1/#tag/Message/operation/cancel-scheduled-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
| `messageId` | path | `string` | yes | Message ID path parameter from the smsmode API route. |
