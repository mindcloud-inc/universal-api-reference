# Wisewand: Create personas

Creates a new persona in your Wisewand workspace.

```
POST https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-personas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-personas" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-personas', {
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
      "created_at": "string",
      "id": "string",
      "last_example": "string",
      "name": "Ava Chen",
      "picture": "string",
      "resume": "string",
      "style": "string",
      "type": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `last_example` | string |  |
| `name` | string |  |
| `picture` | string |  |
| `resume` | string |  |
| `style` | string |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `POST /v1/personas/` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-personas.md) for the provider-specific parameters and requirements.

