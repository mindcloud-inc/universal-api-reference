# CustomerX: List Contract Plans

Retrieves a list of contract plans from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contract-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contract-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contract-plans?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
| `description` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `number_users` | string |  |
| `status` | boolean |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/contract_plans` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contract-plans.md) for the provider-specific parameters and requirements.

