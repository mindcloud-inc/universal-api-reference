# RotaCloud: Create Terminal

Creates a terminal in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-terminal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "timezone": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-terminal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "timezone": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Terminal name. |
| `timezone` | number | yes | Timezone ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "deleted": true,
      "device": "string",
      "id": 1,
      "name": "Ava Chen",
      "require_photo": true,
      "require_photo_breaks": true,
      "secret": "string",
      "timezone": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `deleted` | boolean |  |
| `device` | string |  |
| `id` | number |  |
| `name` | string |  |
| `require_photo` | boolean |  |
| `require_photo_breaks` | boolean |  |
| `secret` | string |  |
| `timezone` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/terminals` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-terminal.md) for the provider-specific parameters and requirements.

