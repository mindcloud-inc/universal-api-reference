# RotaCloud: Get Leave Entry

Retrieves a leave record from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-leave-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-leave-entry?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-leave-entry?${params}`, {
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
| `id` | number | yes | The leave entry identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": 1,
      "admin_message": "string",
      "dates": [
        {}
      ],
      "deleted": true,
      "end_date": "string",
      "hours": {},
      "id": 1,
      "paid": true,
      "replied_at": 1,
      "requested": true,
      "requested_at": 1,
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
| `admin` | number |  |
| `admin_message` | string |  |
| `dates` | array<object> |  |
| `deleted` | boolean |  |
| `end_date` | string |  |
| `hours` | object |  |
| `id` | number |  |
| `paid` | boolean |  |
| `replied_at` | number |  |
| `requested` | boolean |  |
| `requested_at` | number |  |
| `start_date` | string |  |
| `status` | string |  |
| `type` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/leave/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-entry.md) for the provider-specific parameters and requirements.

