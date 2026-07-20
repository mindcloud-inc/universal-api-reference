# Crisp: Get Messages In Conversation

Retrieves messages in a Crisp conversation.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-messages-in-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-messages-in-conversation?connectionId=$CONNECTION_ID&websiteId=string&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-messages-in-conversation?${params}`, {
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
| `websiteId` | string | yes | The website identifier. |
| `sessionId` | string | yes | The conversation session identifier. |
| `timestampBefore` | number | no | Return messages before the given timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automated": true,
      "content": {},
      "delivered": "string",
      "edited": true,
      "fingerprint": 1,
      "from": "string",
      "mentions": [
        "string"
      ],
      "origin": "string",
      "read": "string",
      "sessionId": "string",
      "stamped": true,
      "timestamp": 1,
      "translated": true,
      "type": "string",
      "user": {},
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automated` | boolean |  |
| `content` | object |  |
| `delivered` | string |  |
| `edited` | boolean |  |
| `fingerprint` | number |  |
| `from` | string |  |
| `mentions` | array<string> |  |
| `origin` | string |  |
| `read` | string |  |
| `sessionId` | string |  |
| `stamped` | boolean |  |
| `timestamp` | number |  |
| `translated` | boolean |  |
| `type` | string |  |
| `user` | object |  |
| `websiteId` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/conversation/:session_id/messages` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messages-in-conversation.md) for the provider-specific parameters and requirements.

