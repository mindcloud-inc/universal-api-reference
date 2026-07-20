# Eventee: Create Pause

Creates a pause in Eventee.

```
POST https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-pause
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-pause" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-pause', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "start": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `end` | date |  |
| `id` | number |  |
| `name` | string |  |
| `start` | date |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Eventee API, this operation is `POST /pause` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pause.md) for the provider-specific parameters and requirements.

