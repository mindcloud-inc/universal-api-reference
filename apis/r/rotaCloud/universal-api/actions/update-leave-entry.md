# RotaCloud: Update Leave Entry

Updates a leave record in RotaCloud.

```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-leave-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-leave-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "type": 1,
  "start_date": "string",
  "end_date": "string",
  "users[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-leave-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "type": 1,
    "start_date": "string",
    "end_date": "string",
    "users[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Leave entry ID. |
| `type` | number | yes | Leave type ID. |
| `start_date` | string | yes | Leave entry start date in YYYY-MM-DD format. |
| `end_date` | string | yes | Leave entry end date in YYYY-MM-DD format. |
| `users[]` | array<number> | yes | User IDs on the leave entry. |
| `user` | number | no | Primary user for leave update headers. |

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

Through the native RotaCloud API, this operation is `POST /v1/leave/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-leave-entry.md) for the provider-specific parameters and requirements.

