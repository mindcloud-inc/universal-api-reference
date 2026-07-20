# RotaCloud: Get Leave Request

Retrieves a leave request from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-leave-request?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-leave-request?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The leave request identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dates": [
        {}
      ],
      "deleted": true,
      "end_am_pm": "string",
      "end_date": "string",
      "hours": {},
      "id": 1,
      "paid": true,
      "requested_at": 1,
      "start_am_pm": "string",
      "start_date": "string",
      "status": "string",
      "type": 1,
      "user": 1,
      "user_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dates` | array<object> |  |
| `deleted` | boolean |  |
| `end_am_pm` | string |  |
| `end_date` | string |  |
| `hours` | object |  |
| `id` | number |  |
| `paid` | boolean |  |
| `requested_at` | number |  |
| `start_am_pm` | string |  |
| `start_date` | string |  |
| `status` | string |  |
| `type` | number |  |
| `user` | number |  |
| `user_message` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/leave_requests/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-request.md) for the provider-specific parameters and requirements.

