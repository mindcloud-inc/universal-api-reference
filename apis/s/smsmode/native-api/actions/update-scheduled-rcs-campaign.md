# Update Scheduled RCS Campaign with smsmode

## Endpoint

- **Method:** `PATCH`
- **Path:** `rcs/v1/channels/:channelId/campaigns/:campaignId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Update Scheduled RCS Campaign](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/edit-scheduled-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
| `name` | body | `string` | no | Name request body field documented by the smsmode API. |
| `sentDate` | body | `date` | no | Send Date request body field documented by the smsmode API. |
| `endDate` | body | `date` | no | End Date request body field documented by the smsmode API. |
| `refClient` | body | `string` | no | Client Reference request body field documented by the smsmode API. |
| `callbackUrlStatus` | body | `string` | no | Status Callback URL request body field documented by the smsmode API. |
| `callbackUrlMo` | body | `string` | no | MO Callback URL request body field documented by the smsmode API. |
