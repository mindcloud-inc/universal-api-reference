# Twitch: Create Poll

Creates a new poll in Twitch.

```
POST https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-poll
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-poll" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "title": "string",
  "choices[].title": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-poll', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "title": "string",
    "choices[].title": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | ID of the broadcaster that owns the poll. Must match the user in the OAuth token. |
| `title` | string | yes | Question shown at the top of the poll. |
| `choices[].title` | string | yes | Choice title. Provide 2 to 5 values to build the choices array. Accepts multiple values as an array. |
| `duration` | number | yes | Poll duration in seconds. |
| `channelPointsVotingEnabled` | boolean | no | Set to true to let viewers vote with Channel Points. |
| `channelPointsPerVote` | number | no | Number of Channel Points required per additional vote. Required when channel_points_voting_enabled is true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "bitsPerVote": 1,
          "bitsVotingEnabled": true,
          "broadcasterId": "string",
          "broadcasterLogin": "string",
          "broadcasterName": "Ava Chen",
          "channelPointsPerVote": 1,
          "channelPointsVotingEnabled": true,
          "choices": [
            {
              "bitsVotes": 1,
              "channelPointsVotes": 1,
              "id": "string",
              "title": "string",
              "votes": 1
            }
          ],
          "duration": 1,
          "endedAt": "string",
          "id": "string",
          "startedAt": "string",
          "status": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Poll rows. |
| `data[].bitsPerVote` | number | Bits cost per vote. |
| `data[].bitsVotingEnabled` | boolean | Whether bits voting is enabled. |
| `data[].broadcasterId` | string | Broadcaster identifier. |
| `data[].broadcasterLogin` | string | Broadcaster login name. |
| `data[].broadcasterName` | string | Broadcaster display name. |
| `data[].channelPointsPerVote` | number | Channel points cost per vote. |
| `data[].channelPointsVotingEnabled` | boolean | Whether channel points voting is enabled. |
| `data[].choices` | array<object> | Poll choice rows. |
| `data[].choices[].bitsVotes` | number | Bits votes for the choice. |
| `data[].choices[].channelPointsVotes` | number | Channel points votes for the choice. |
| `data[].choices[].id` | string | Poll choice identifier. |
| `data[].choices[].title` | string | Poll choice title. |
| `data[].choices[].votes` | number | Total votes for the choice. |
| `data[].duration` | number | Poll duration in seconds. |
| `data[].endedAt` | string | Timestamp when the poll ended. |
| `data[].id` | string | Poll identifier. |
| `data[].startedAt` | string | Timestamp when the poll started. |
| `data[].status` | string | Poll status. |
| `data[].title` | string | Poll question. |

## Native endpoint

Through the native Twitch API, this operation is `POST /polls` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-poll.md) for the provider-specific parameters and requirements.

