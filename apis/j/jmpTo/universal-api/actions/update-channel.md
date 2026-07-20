# JmpTo: Update Channel

Updates an existing channel in JmpTo.

```
PUT https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Channel ID to update. |
| `name` | string | no | Channel name. |
| `description` | string | no | Channel description. |
| `color` | string | no | Channel badge color in HEX format. |
| `starred` | boolean | no | Whether to star the channel. |

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
| `color` | string | Channel color. |
| `description` | string | Channel description. |
| `error` | number | Provider success/error code. |
| `id` | number | Channel ID. |
| `name` | string | Channel name. |
| `starred` | boolean | Whether the channel is starred. |

## Native endpoint

Through the native JmpTo API, this operation is `PUT /channel/:id/update` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

