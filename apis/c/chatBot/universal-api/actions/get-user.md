# ChatBot: Get User

Retrieves user details from ChatBot API.

```
GET https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-user?connectionId=$CONNECTION_ID&id=69bae98566f10f0007c4e5eb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "69bae98566f10f0007c4e5eb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The required ChatBot user ID from the request path. Example: `69bae98566f10f0007c4e5eb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "banned": true,
      "conversations": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "sessionAttributes": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `banned` | boolean |  |
| `conversations` | array<object> |  |
| `createdAt` | date |  |
| `id` | string |  |
| `lastSeen` | date |  |
| `sessionAttributes` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native ChatBot API, this operation is `GET /users/:id` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

