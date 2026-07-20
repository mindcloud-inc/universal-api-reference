# End Poll with Twitch

Ends an existing poll in Twitch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/polls`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [End Poll](https://dev.twitch.tv/docs/api/reference#end-poll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | body | `string` | yes | ID of the broadcaster that owns the poll. Must match the user in the OAuth token. |
| `id` | body | `string` | yes | ID of the poll to end. |
| `status` | body | `string` | yes | How to end the poll. Use TERMINATED or ARCHIVED. Accepted values: `ARCHIVED`, `TERMINATED`. |
