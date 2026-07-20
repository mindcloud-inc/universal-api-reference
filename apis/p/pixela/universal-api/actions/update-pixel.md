# Pixela: Update Pixel

Updates a pixel in Pixela, or creates it if missing.

```
PUT https://connect.mindcloud.co/v1/universal/pixela/latest/actions/update-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/update-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "graph_id": "string",
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixela/latest/actions/update-pixel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "graph_id": "string",
    "date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quantity` | string | no | Quantity to set for the pixel. |
| `username` | string | yes | Pixela username in the request path. |
| `graph_id` | string | yes | Pixela graph identifier. |
| `date` | string | yes | Pixel date in yyyyMMdd format. |

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

Through the native Pixela API, this operation is `PUT /v1/users/:username/graphs/:graphID/:yyyyMMdd` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pixel.md) for the provider-specific parameters and requirements.

