# Send SMS Message with smsmode

## Endpoint

- **Method:** `POST`
- **Path:** `sms/v1/channels/:channelId/campaigns/:campaignId/messages`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Send SMS Message](https://dev.smsmode.com/sms/v1/#tag/Message/operation/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
| `recipient` | body | `object` | yes | Recipient request body field documented by the smsmode API. |
| `body` | body | `object` | yes | Body request body field documented by the smsmode API. |
| `from` | body | `string` | no | Sender request body field documented by the smsmode API. |
| `sentDate` | body | `date` | no | Send Date request body field documented by the smsmode API. |
| `refClient` | body | `string` | no | Client Reference request body field documented by the smsmode API. |
| `callbackUrlStatus` | body | `string` | no | Status Callback URL request body field documented by the smsmode API. |
| `callbackUrlMo` | body | `string` | no | MO Callback URL request body field documented by the smsmode API. |
