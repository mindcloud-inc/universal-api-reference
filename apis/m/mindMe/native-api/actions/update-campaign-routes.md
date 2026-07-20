# Update Campaign Routes with MindMe

Updates campaign routes in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Campaign/SaveCampaignRoutes`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Update Campaign Routes](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1SaveCampaignRoutes/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | no |
| `campaignId` | body | `string` | no |
| `isEmailRoute` | body | `string` | no |
| `isSmsRoute` | body | `string` | no |
