# Get Live Chat Status Counts with Instabot

Retrieves live chat status counts from Instabot.

## Endpoint

- **Method:** `POST`
- **Path:** `/instabot/chats/liveChatStatusCounts`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [Get Live Chat Status Counts](https://docs.instabot.io/reference/post_instabot-chats-livechatstatuscounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchString` | body | `string` | no | Text used to filter chat status counts. |
| `startDate` | body | `date` | no | Start of the date window for live chat status counts. |
| `endDate` | body | `date` | no | End of the date window for live chat status counts. |
| `botDeletionStatus` | body | `string` | no | Filter counts by bot deletion status. |
