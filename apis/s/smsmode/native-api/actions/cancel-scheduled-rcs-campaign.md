# Cancel Scheduled RCS Campaign with smsmode

## Endpoint

- **Method:** `DELETE`
- **Path:** `rcs/v1/channels/:channelId/campaigns/:campaignId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Cancel Scheduled RCS Campaign](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/cancel-scheduled-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
