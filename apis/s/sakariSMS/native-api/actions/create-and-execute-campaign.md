# Create And Execute Campaign with Sakari SMS

Creates and launches a campaign in Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/quickcampaigns`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Create And Execute Campaign](https://developer.sakari.io/api-reference/campaigns/create-and-execute-a-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `groupId` | body | `string` | yes |
| `listId` | body | `string` | yes |
| `message` | body | `object` | yes |
| `message.message` | body | `string` | no |
| `message.media[]` | body | `array<object>` | no |
| `message.media.media[].url` | body | `string` | no |
| `message.media.media[].type` | body | `string` | no |
| `message.media.media[].name` | body | `string` | no |
| `message.media.media[].filename` | body | `string` | no |
| `sendAt` | body | `date` | no |
