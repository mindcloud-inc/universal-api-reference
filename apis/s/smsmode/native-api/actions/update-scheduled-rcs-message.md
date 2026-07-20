# Update Scheduled RCS Message with smsmode

## Endpoint

- **Method:** `PATCH`
- **Path:** `rcs/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Update Scheduled RCS Message](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/edit-scheduled-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
| `messageId` | path | `string` | yes | Message ID path parameter from the smsmode API route. |
| `recipient` | body | `object` | no | Recipient request body field documented by the smsmode API. |
| `sentDate` | body | `date` | no | Send Date request body field documented by the smsmode API. |
| `refClient` | body | `string` | no | Client Reference request body field documented by the smsmode API. |
| `callbackUrlStatus` | body | `string` | no | Status Callback URL request body field documented by the smsmode API. |
| `callbackUrlMo` | body | `string` | no | MO Callback URL request body field documented by the smsmode API. |
