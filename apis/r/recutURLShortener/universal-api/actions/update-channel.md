# Recut URL Shortener: Update Channel

Updates an existing channel in Recut URL Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Updated Channel Name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Updated Channel Name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Channel ID. |
| `name` | string | yes | Channel name. Example: `Updated Channel Name`. |
| `description` | string | no | Channel description. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | Channel badge color in hex format. |
| `starred` | boolean | no | Whether the channel is starred. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "description": "string",
      "error": 1,
      "id": 1,
      "name": "Ava Chen",
      "starred": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Channel badge color. |
| `description` | string | Channel description. |
| `error` | number | Recut API error flag. |
| `id` | number | Updated channel ID. |
| `name` | string | Channel name. |
| `starred` | boolean | Whether the channel is starred. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `PUT /channel/:id/update` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

