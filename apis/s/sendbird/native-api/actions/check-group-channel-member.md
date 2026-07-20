# Check Group Channel Member with Sendbird

## Endpoint

- **Method:** `GET`
- **Path:** `/group_channels/:channelUrl/members/:userId`
- **Base URL:** `https://api-{applicationId}.sendbird.com/v3`
- **Official documentation:** [Check Group Channel Member](https://docs.sendbird.com/docs/chat/platform-api/v3/channel/managing-members/check-if-user-is-a-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_url` | path | `string` | yes | The group channel URL. |
| `user_id` | path | `string` | yes | The user ID. |
