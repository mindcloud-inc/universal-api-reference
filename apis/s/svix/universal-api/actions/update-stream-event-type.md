# Svix: Update Stream Event Type

Creates or updates a stream event type in Svix.

```
PUT https://connect.mindcloud.co/v1/universal/svix/latest/actions/update-stream-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/svix/latest/actions/update-stream-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/update-stream-event-type', {
  method: 'PUT',
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

Through the native Svix API, this operation is `PUT /api/v1/stream/event-type/{name}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-stream-event-type.md) for the provider-specific parameters and requirements.

