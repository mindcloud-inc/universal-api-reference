# RotaCloud: Create Location

Creates a location in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-location', {
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
| `name` | string | yes | Location name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "clock_in_ips": [
        "string"
      ],
      "deleted": true,
      "id": 1,
      "location": {},
      "managers": [
        1
      ],
      "metadata": {},
      "name": "Ava Chen",
      "timezone": 1,
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
| `address` | string |  |
| `clock_in_ips` | array<string> |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `location` | object |  |
| `managers` | array<number> |  |
| `metadata` | object |  |
| `name` | string |  |
| `timezone` | number |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/locations` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

