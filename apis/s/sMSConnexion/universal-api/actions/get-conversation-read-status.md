# SMS Connexion: Get Conversation Read Status



```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-conversation-read-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-conversation-read-status?connectionId=$CONNECTION_ID&conversationId=9d50be59-158d-4a6d-ae4a-8ca6ba63f69e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "9d50be59-158d-4a6d-ae4a-8ca6ba63f69e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-conversation-read-status?${params}`, {
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
      "id": "string",
      "info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `info` | object |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /conversations/:conversationId/read` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-read-status.md) for the provider-specific parameters and requirements.

