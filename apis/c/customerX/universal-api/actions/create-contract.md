# CustomerX: Create Contract

Creates a new contract in CustomerX.

```
POST https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract', {
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
      "auto_renovation": true,
      "cancellation_date": "string",
      "cancellation_reason": "string",
      "contract_value": "string",
      "date_sale": "string",
      "description": "string",
      "external_id_contract": "string",
      "final_date": "string",
      "id": 1,
      "initial_date_sale": "string",
      "initial_final_date": "string",
      "initial_start_date": "string",
      "initial_value": "string",
      "number_of_users": 1,
      "renew_in_days": 1,
      "start_date": "string",
      "status": "string",
      "value_per_user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_renovation` | boolean |  |
| `cancellation_date` | string |  |
| `cancellation_reason` | string |  |
| `contract_value` | string |  |
| `date_sale` | string |  |
| `description` | string |  |
| `external_id_contract` | string |  |
| `final_date` | string |  |
| `id` | number |  |
| `initial_date_sale` | string |  |
| `initial_final_date` | string |  |
| `initial_start_date` | string |  |
| `initial_value` | string |  |
| `number_of_users` | number |  |
| `renew_in_days` | number |  |
| `start_date` | string |  |
| `status` | string |  |
| `value_per_user` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/contracts` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract.md) for the provider-specific parameters and requirements.

