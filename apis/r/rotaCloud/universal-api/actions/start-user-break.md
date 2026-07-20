# RotaCloud: Start User Break



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/start-user-break
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/start-user-break" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "id": 1,
  "method": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/start-user-break', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "id": 1,
    "method": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Break action name. |
| `id` | number | yes | User ID on break. |
| `method` | string | yes | Break start method. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breaks_clocked": [
        {}
      ],
      "in_device": "string",
      "in_location": {},
      "in_method": "string",
      "in_terminal": 1,
      "in_time": 1,
      "location": 1,
      "minutes_late": 1,
      "role": 1,
      "shift": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breaks_clocked` | array<object> |  |
| `in_device` | string |  |
| `in_location` | object |  |
| `in_method` | string |  |
| `in_terminal` | number |  |
| `in_time` | number |  |
| `location` | number |  |
| `minutes_late` | number |  |
| `role` | number |  |
| `shift` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/users_clocked_in/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-user-break.md) for the provider-specific parameters and requirements.

