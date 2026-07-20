# Octadesk: List Chat Events

Retrieves events from an Octadesk chat.

```
GET https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chat-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chat-events?connectionId=$CONNECTION_ID&id=07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chat-events?${params}`, {
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
| `id` | string | yes | Chat ID from Octadesk. Example: `07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `time` | date |  |
| `type` | string |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |

## Native endpoint

Through the native Octadesk API, this operation is `GET /chat/:id/events` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-events.md) for the provider-specific parameters and requirements.

