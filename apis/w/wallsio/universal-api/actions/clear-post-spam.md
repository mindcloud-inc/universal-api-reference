# Walls.io: Clear Post Spam

Clears a post spam status in Walls.io.

```
PUT https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/clear-post-spam
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walls.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/clear-post-spam" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/clear-post-spam', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postId` | string | no | Walls.io post ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_time": 1,
      "data": {},
      "info": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_time` | number |  |
| `data` | object |  |
| `info` | array<string> |  |

## Native endpoint

Through the native Walls.io API, this operation is `PUT /posts/:postId` (base URL `https://api.walls.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-post-spam.md) for the provider-specific parameters and requirements.

