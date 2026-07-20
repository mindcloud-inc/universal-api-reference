# Morningmate: Invite Participants to Chat Room

Invites participants to a Morningmate chat room.

```
PUT https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/invite-participants-to-chat-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/invite-participants-to-chat-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "12345",
  "registerId": "apps@mindcloud.co",
  "participants[]": [
    {}
  ],
  "participants[].participantId": "colleague@company.name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/invite-participants-to-chat-room', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "12345",
    "registerId": "apps@mindcloud.co",
    "participants[]": [{}],
    "participants[].participantId": "colleague@company.name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Morningmate numeric chat room ID Example: `12345`. |
| `registerId` | string | yes | Morningmate author user ID Example: `apps@mindcloud.co`. |
| `participants[]` | array<object> | yes | Participants array |
| `participants[].participantId` | string | yes | Participant ID to invite Example: `colleague@company.name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roomId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roomId` | string |  |

## Native endpoint

Through the native Morningmate API, this operation is `POST /v1/chats/[:roomId]/participants` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-participants-to-chat-room.md) for the provider-specific parameters and requirements.

