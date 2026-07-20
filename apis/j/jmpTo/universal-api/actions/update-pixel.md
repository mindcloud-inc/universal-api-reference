# JmpTo: Update Pixel

Updates an existing pixel in JmpTo.

```
PUT https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-pixel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Pixel ID to update. |
| `name` | string | no | Custom name for the pixel. |
| `tag` | string | yes | The tag for the pixel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number | Provider success/error code. |
| `message` | string | Update result message. |

## Native endpoint

Through the native JmpTo API, this operation is `PUT /pixel/:id/update` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pixel.md) for the provider-specific parameters and requirements.

