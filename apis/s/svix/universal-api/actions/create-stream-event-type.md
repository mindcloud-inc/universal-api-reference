# Svix: Create Stream Event Type

Creates a stream event type in Svix.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-stream-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-stream-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-stream-event-type', {
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
      "archived": true,
      "createdAt": "string",
      "deprecated": true,
      "description": "string",
      "featureFlags": [
        "string"
      ],
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `deprecated` | boolean |  |
| `description` | string |  |
| `featureFlags` | array<string> |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Svix API, this operation is `POST /api/v1/stream/event-type` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-stream-event-type.md) for the provider-specific parameters and requirements.

