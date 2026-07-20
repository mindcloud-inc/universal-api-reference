# SMS Connexion: List Conversations

Retrieves conversations from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/list-conversations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "countryIso": "string",
      "data": [
        "string"
      ],
      "firstName": "Ava",
      "lastName": "Chen",
      "lastReply": "string",
      "lastUpdate": "string",
      "phoneNumber": "string",
      "unreadMessages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | string |  |
| `countryIso` | string |  |
| `data` | array |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `lastReply` | string |  |
| `lastUpdate` | string |  |
| `phoneNumber` | string |  |
| `unreadMessages` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /conversations` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

