# Superchat: Get Inbox

Retrieves an inbox from Superchat by ID.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-inbox?connectionId=$CONNECTION_ID&inbox_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inbox_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-inbox?${params}`, {
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
| `inbox_id` | string | yes | The id of the inbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "users": {
        "email": "ava@example.com",
        "id": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `url` | string |  |
| `users` | array<object> |  |
| `users.email` | string |  |
| `users.id` | string |  |
| `users.url` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `GET /inboxes/{inbox_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox.md) for the provider-specific parameters and requirements.

