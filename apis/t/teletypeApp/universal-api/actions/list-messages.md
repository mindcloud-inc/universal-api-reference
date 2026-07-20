# Teletype App: List Messages

Retrieves all messages from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-messages?${params}`, {
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
      "createdAt": {},
      "dialogId": "string",
      "id": "string",
      "isItClient": true,
      "provider": 1,
      "seen": true,
      "sentAt": {},
      "sessionId": "string",
      "status": 1,
      "text": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | object |  |
| `dialogId` | string |  |
| `id` | string |  |
| `isItClient` | boolean |  |
| `provider` | number |  |
| `seen` | boolean |  |
| `sentAt` | object |  |
| `sessionId` | string |  |
| `status` | number |  |
| `text` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /messages` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

