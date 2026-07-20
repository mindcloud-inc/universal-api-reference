# MessageBird: Get Conversation



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation?connectionId=$CONNECTION_ID&workspaceId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation?${params}`, {
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
| `conversationId` | string | yes | The Bird conversation ID you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibility": "string",
      "activeParticipantCount": 1,
      "attributes": {},
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "featuredParticipants": [
        {}
      ],
      "hasDraft": true,
      "id": "string",
      "initiatingParticipant": {},
      "lastMessage": {},
      "lastMessageIncomingAt": "2026-05-07T12:00:00.000Z",
      "lastMessageOutgoingAt": "2026-05-07T12:00:00.000Z",
      "likelySpam": true,
      "likelySpamReason": "string",
      "name": "Ava Chen",
      "pendingParticipantCount": 1,
      "platformStyle": "string",
      "referral": {},
      "resource": {},
      "status": "string",
      "style": "string",
      "summary": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibility` | string | Indicates the access level for new participants to join the conversation. |
| `activeParticipantCount` | number | Number of active participants. |
| `attributes` | object | A free-form object containing conversation attributes. You can use this field to store custom information along with the conversation. |
| `channelId` | string | Channel ID. |
| `createdAt` | date | Creation timestamp formatted as RFC3339. |
| `description` | string | Conversation description. |
| `featuredParticipants` | array<object> | A list of up to 5 conversation participants. |
| `hasDraft` | boolean | Indicates if the conversation contains at least one draft message. |
| `id` | string | Conversation ID. |
| `initiatingParticipant` | object | A participant who can send and receive messages in the conversation |
| `lastMessage` | object | Last message sent in this conversation. |
| `lastMessageIncomingAt` | date | Timestamp of the last incoming message in RFC3339 format. |
| `lastMessageOutgoingAt` | date | Timestamp of the last outgoing message in RFC3339 format. |
| `likelySpam` | boolean | Whether this conversation was flagged as spam. Only present when anti-spam is enabled in the workspace settings. |
| `likelySpamReason` | string | Reason for being flagged as spam. |
| `name` | string | Name of the conversation. If it's an email channel, this will correspond to the email subject. |
| `pendingParticipantCount` | number | Number of participants who have requested to join the conversation with pending approval. |
| `platformStyle` | string | The communication style of the platform. `email` represents an email channel; `direct` represents a 1:1 conversation, most channels will fall in this category, like WhatsApp and RCS; `direct-multiple` represents a channel that supports multiple conversations per contact, e.g. Chat; `direct-threaded` represents a threaded communication channel, e.g. Instagram Comments. |
| `referral` | object | This represents a social media post or an ad that was referenced when starting the conversation. |
| `resource` | object | Resource reference |
| `status` | string | Status of the conversation. Attempting to send messages in closed conversations results in an error. |
| `style` | string | The style of the conversation. - `default`: The conversation style is dictated by the underlying platform. Participants will be a mix of user and contact participants. - `directMessage`: The conversation is a direct conversation between user participants. Participants will be of user type. - `chatChannel`: The conversation is a chat channel conversation. Participants will be of user type. - `personalInbox`: The conversation is in the personal inbox for a user participant. Participants will be the owning user, and one or more personal contact participants. - `resource`: The conversation consists of comments on a resource. Participants will be of user type and `resource` will be set. |
| `summary` | string | Summary of the conversation. |
| `updatedAt` | date | Update timestamp formatted as RFC3339. |
| `visibility` | string | Whether the conversation is public or private. |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/conversations/:conversationId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

