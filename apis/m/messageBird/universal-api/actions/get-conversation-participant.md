# MessageBird: Get Conversation Participant



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation-participant?connectionId=$CONNECTION_ID&workspaceId=string&conversationId=string&conversationParticipantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "conversationId": "string",
  "conversationParticipantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation-participant?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | string | yes | The Bird conversation ID that owns the participant. |
| `conversationParticipantId` | string | yes | The Bird conversation participant ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "contact": {},
      "displayName": "Ava Chen",
      "id": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string | An URL to the participant's avatar. |
| `contact` | object | The participant's contact information. For more information on identifier keys and values, please refer to the "Conversation Participants" page. |
| `displayName` | string | The participant's name. |
| `id` | string | Participant ID, the meaning of this field depends on `type`. If `type` is `user` then it's a user ID, if `type` is `contact` then it's a contact ID, if `type` is `accessKey` then it's the access key ID, and so on. |
| `status` | string | Participant status in the conversation. `pending` means it's pending approval, `invited` means it's pending acceptance from the participant, and `active` means the participant can send and receive messages. |
| `type` | string | Participant type. The main ones are `user`, `contact`, and `agent`. `user` is a user belonging to your Bird workspace, `contact` is one of your customers, `agent` is a customer service agent, and the remaining types represent system participants. |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/conversations/:conversationId/participants/:conversationParticipantId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-participant.md) for the provider-specific parameters and requirements.

