# Instructure: List Communication Channels

Retrieves communication channels from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-communication-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-communication-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-communication-channels?${params}`, {
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
      "address": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "position": 1,
      "type": "string",
      "user_id": 1,
      "workflow_state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `position` | number |  |
| `type` | string |  |
| `user_id` | number |  |
| `workflow_state` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self/communication_channels` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-communication-channels.md) for the provider-specific parameters and requirements.

