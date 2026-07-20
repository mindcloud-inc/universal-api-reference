# Hey Reach: Get Conversation

Retrieves a LinkedIn conversation from Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-conversation?connectionId=$CONNECTION_ID&accountId=1&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-conversation?${params}`, {
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
| `accountId` | number | yes |  |
| `conversationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockedByMe": "string",
      "blockedByParticipant": "string",
      "campaignId": "string",
      "correspondentProfile": {},
      "groupChat": "string",
      "id": "string",
      "lastMessageAt": "string",
      "lastMessageSender": "string",
      "lastMessageText": "string",
      "linkedInAccount": {},
      "linkedInAccountId": "https://example.com",
      "messages": [
        {}
      ],
      "read": "string",
      "totalMessages": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockedByMe` | string |  |
| `blockedByParticipant` | string |  |
| `campaignId` | string |  |
| `correspondentProfile` | object |  |
| `groupChat` | string |  |
| `id` | string |  |
| `lastMessageAt` | string |  |
| `lastMessageSender` | string |  |
| `lastMessageText` | string |  |
| `linkedInAccount` | object |  |
| `linkedInAccountId` | string |  |
| `messages` | array<object> |  |
| `read` | string |  |
| `totalMessages` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `GET /api/public/inbox/GetChatroom/:accountId/:conversationId` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

