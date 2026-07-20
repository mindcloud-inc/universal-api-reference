# Create Poll with Twitch

Creates a new poll in Twitch.

## Endpoint

- **Method:** `POST`
- **Path:** `/polls`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Create Poll](https://dev.twitch.tv/docs/api/reference#create-poll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | body | `string` | yes | ID of the broadcaster that owns the poll. Must match the user in the OAuth token. |
| `title` | body | `string` | yes | Question shown at the top of the poll. |
| `choices[].title` | body | `string` | yes | Choice title. Provide 2 to 5 values to build the choices array. Send multiple values as a array. |
| `duration` | body | `number` | yes | Poll duration in seconds. |
| `channel_points_voting_enabled` | body | `boolean` | no | Set to true to let viewers vote with Channel Points. |
| `channel_points_per_vote` | body | `number` | no | Number of Channel Points required per additional vote. Required when channel_points_voting_enabled is true. |
