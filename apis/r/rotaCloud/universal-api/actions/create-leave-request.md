# RotaCloud: Create Leave Request

Requests leave in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-leave-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "end_date": "string",
  "start_date": "string",
  "type": 1,
  "user": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-leave-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "end_date": "string",
    "start_date": "string",
    "type": 1,
    "user": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end_date` | string | yes | Leave request end date in ISO format. |
| `start_date` | string | yes | Leave request start date in ISO format. |
| `type` | number | yes | Leave type ID. |
| `user` | number | yes | User ID requesting leave. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dates": [
        {}
      ],
      "end_date": "string",
      "hours": {},
      "id": 1,
      "paid": true,
      "start_date": "string",
      "status": "string",
      "type": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dates` | array<object> |  |
| `end_date` | string |  |
| `hours` | object |  |
| `id` | number |  |
| `paid` | boolean |  |
| `start_date` | string |  |
| `status` | string |  |
| `type` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/leave_requests` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-leave-request.md) for the provider-specific parameters and requirements.

