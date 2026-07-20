# SMS Connexion: Get Conversation

Retrieves a conversation from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-conversation?connectionId=$CONNECTION_ID&conversationId=9d50be59-158d-4a6d-ae4a-8ca6ba63f69e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "9d50be59-158d-4a6d-ae4a-8ca6ba63f69e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-conversation?${params}`, {
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
| `conversationId` | string | yes | Conversation UUID. Example: `9d50be59-158d-4a6d-ae4a-8ca6ba63f69e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "conversationId": "string",
      "cost": 1,
      "countryIso": "string",
      "data": [
        "string"
      ],
      "datetime": "string",
      "firstName": "Ava",
      "info": {},
      "lastName": "Chen",
      "msgId": "string",
      "phoneNumber": "string",
      "richMedia": {},
      "status": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `conversationId` | string |  |
| `cost` | number |  |
| `countryIso` | string |  |
| `data` | array |  |
| `datetime` | string |  |
| `firstName` | string |  |
| `info` | object |  |
| `lastName` | string |  |
| `msgId` | string |  |
| `phoneNumber` | string |  |
| `richMedia` | object |  |
| `status` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /conversations/:conversationId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

