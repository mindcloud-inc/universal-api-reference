# Pixela: Decrement Pixel

Decrements today's pixel in Pixela using the graph timezone.

```
PUT https://connect.mindcloud.co/v1/universal/pixela/latest/actions/decrement-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/decrement-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "graph_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixela/latest/actions/decrement-pixel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "graph_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Pixela username in the request path. |
| `graph_id` | string | yes | Pixela graph identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isSuccess": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSuccess` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Pixela API, this operation is `PUT /v1/users/:username/graphs/:graphID/decrement` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decrement-pixel.md) for the provider-specific parameters and requirements.

