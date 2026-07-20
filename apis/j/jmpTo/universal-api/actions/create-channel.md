# JmpTo: Create Channel

Creates a channel in JmpTo.

```
POST https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Channel name. |
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

Through the native JmpTo API, this operation is `POST /channel/add` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

