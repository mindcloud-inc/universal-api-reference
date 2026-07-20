# RotaCloud: Update Terminal

Updates a terminal in RotaCloud.

```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-terminal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-terminal', {
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
| `id` | number | yes | Terminal ID. |

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

Through the native RotaCloud API, this operation is `POST /v1/terminals/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-terminal.md) for the provider-specific parameters and requirements.

