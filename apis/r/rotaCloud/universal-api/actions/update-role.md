# RotaCloud: Update Role

Updates a role in RotaCloud.

```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-role', {
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
| `id` | number | yes | Role ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colour": "string",
      "default_break": 1,
      "deleted": true,
      "id": 1,
      "name": "Ava Chen",
      "pay_code": "string",
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colour` | string |  |
| `default_break` | number |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `pay_code` | string |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/roles/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-role.md) for the provider-specific parameters and requirements.

