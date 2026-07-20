# Cliengo: List Conversation Messages



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-conversation-messages?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-conversation-messages?${params}`, {
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
| `conversationId` | string | yes | Identifier of the Cliengo conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "id": "string",
      "message": {},
      "response_options": [
        {}
      ],
      "sendAt": "2026-05-07T12:00:00.000Z",
      "sender": {},
      "sentAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `id` | string |  |
| `message` | object |  |
| `response_options` | array<object> |  |
| `sendAt` | date |  |
| `sender` | object |  |
| `sentAt` | date |  |
| `tags` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /conversations/:conversationId/messages` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-messages.md) for the provider-specific parameters and requirements.

