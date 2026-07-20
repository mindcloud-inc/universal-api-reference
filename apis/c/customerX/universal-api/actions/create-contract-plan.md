# CustomerX: Create Contract Plan

Creates a new contract plan in CustomerX.

```
POST https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "deleted_at": "string",
      "description": "string",
      "external_id": "string",
      "id": 1,
      "number_users": "string",
      "status": true,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `deleted_at` | string |  |
| `description` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `number_users` | string |  |
| `status` | boolean |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/contract_plans` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract-plan.md) for the provider-specific parameters and requirements.

