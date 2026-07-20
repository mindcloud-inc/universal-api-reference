# Crisp: Get Conversation Metas

Retrieves a conversation's metadata from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-conversation-metas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-conversation-metas?connectionId=$CONNECTION_ID&websiteId=string&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-conversation-metas?${params}`, {
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
| `websiteId` | string | yes | The website identifier |
| `sessionId` | string | yes | The conversation session identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "avatar": "string",
      "connection": {},
      "data": {},
      "device": {},
      "email": "ava@example.com",
      "ip": "string",
      "nickname": "Ava Chen",
      "origin": "string",
      "phone": "string",
      "segments": [
        "string"
      ],
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `avatar` | string |  |
| `connection` | object |  |
| `data` | object |  |
| `device` | object |  |
| `email` | string |  |
| `ip` | string |  |
| `nickname` | string |  |
| `origin` | string |  |
| `phone` | string |  |
| `segments` | array<string> |  |
| `subject` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/conversation/:session_id/meta` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-metas.md) for the provider-specific parameters and requirements.

