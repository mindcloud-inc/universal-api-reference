# CustomerX: Update Contract By External ID

Updates an existing contract in CustomerX by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-contract-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-contract-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-contract-by-external-id', {
  method: 'PUT',
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
      "client_id": 1,
      "contract_value": "string",
      "date_sale": "string",
      "description": "string",
      "external_id_contract": "string",
      "final_date": "string",
      "id": 1,
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
| `client_id` | number |  |
| `contract_value` | string |  |
| `date_sale` | string |  |
| `description` | string |  |
| `external_id_contract` | string |  |
| `final_date` | string |  |
| `id` | number |  |
| `initial_final_date` | string |  |
| `initial_start_date` | string |  |
| `initial_value` | string |  |
| `number_of_users` | number |  |
| `renew_in_days` | number |  |
| `start_date` | string |  |
| `status` | string |  |
| `value_per_user` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `PUT /api/v1/contracts` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contract-by-external-id.md) for the provider-specific parameters and requirements.

