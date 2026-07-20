# Create Campaign with MindMe

Creates a new campaign in MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Campaign/SaveCampaign`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [Create Campaign](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Campaign~1SaveCampaign/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | no |
| `fromEmail` | body | `string` | no |
| `isEmailCampaign` | body | `string` | no |
| `isSmsCampaign` | body | `string` | no |
| `name` | body | `string` | no |
| `subject` | body | `string` | no |
