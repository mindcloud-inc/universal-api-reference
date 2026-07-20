# Habitica: List Inbox Messages

Retrieves inbox messages from Habitica.

```
GET https://connect.mindcloud.co/v1/universal/habitica/latest/actions/list-inbox-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/list-inbox-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/habitica/latest/actions/list-inbox-messages?${params}`, {
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
      "id": "string",
      "text": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `text` | string |  |
| `timestamp` | date |  |
| `username` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Habitica API, this operation is `GET /inbox/messages` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inbox-messages.md) for the provider-specific parameters and requirements.

