# RotaCloud: Create Leave Embargo

Creates a leave embargo in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-leave-embargo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-leave-embargo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "end_date": "string",
  "start_date": "string",
  "users[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-leave-embargo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "end_date": "string",
    "start_date": "string",
    "users[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end_date` | string | yes | Embargo end date in ISO format. |
| `start_date` | string | yes | Embargo start date in ISO format. |
| `users[]` | array<number> | yes | User IDs covered by the embargo. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_am_pm": "string",
      "end_date": "string",
      "everyone": true,
      "id": 1,
      "message": "string",
      "start_am_pm": "string",
      "start_date": "string",
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
| `end_am_pm` | string |  |
| `end_date` | string |  |
| `everyone` | boolean |  |
| `id` | number |  |
| `message` | string |  |
| `start_am_pm` | string |  |
| `start_date` | string |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/leave_embargoes` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-leave-embargo.md) for the provider-specific parameters and requirements.

