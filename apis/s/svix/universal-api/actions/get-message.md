# Svix: Get Message

Retrieves a message from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-message?${params}`, {
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
      "channels": [
        "string"
      ],
      "deliverAt": "string",
      "eventId": "string",
      "eventType": "string",
      "id": "string",
      "payload": {},
      "tags": [
        "string"
      ],
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<string> |  |
| `deliverAt` | string |  |
| `eventId` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `payload` | object |  |
| `tags` | array<string> |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/app/{app_id}/msg/{msg_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

