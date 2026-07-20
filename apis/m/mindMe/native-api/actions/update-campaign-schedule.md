# Update Campaign Schedule with MindMe

Updates a campaign schedule in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Campaign/SaveCampaignScheduling`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Update Campaign Schedule](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1SaveCampaignScheduling/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | no |
| `campaignId` | body | `string` | no |
| `campaignScheduleType` | body | `string` | no |
| `scheduleDate` | body | `string` | no |
