# RotaCloud: Create TOIL Accrual

Creates a toil accrual record in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-toil-accrual
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-toil-accrual" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "duration_hours": 1,
  "leave_year": 1,
  "user_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-toil-accrual', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "duration_hours": 1,
    "leave_year": 1,
    "user_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration_hours` | number | yes | TOIL duration in hours. |
| `leave_year` | number | yes | Leave year for the accrual. |
| `user_id` | number | yes | User receiving the accrual. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "created_at": 1,
      "created_by": 1,
      "date": "string",
      "deleted": true,
      "deleted_at": "string",
      "deleted_by": 1,
      "duration_hours": 1,
      "id": 1,
      "leave_year": 1,
      "location_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `created_at` | number |  |
| `created_by` | number |  |
| `date` | string |  |
| `deleted` | boolean |  |
| `deleted_at` | string |  |
| `deleted_by` | number |  |
| `duration_hours` | number |  |
| `id` | number |  |
| `leave_year` | number |  |
| `location_id` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/toil_accruals` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-toil-accrual.md) for the provider-specific parameters and requirements.

