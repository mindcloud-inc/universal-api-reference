# CustomerX: Create Contract Additive

Creates a new contract additive in CustomerX.

```
POST https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract-additive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract-additive" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-contract-additive', {
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
      "client_contract_id": 1,
      "client_id": 1,
      "created_at": "string",
      "date_final": "string",
      "date_initial": "string",
      "date_sale": "string",
      "description": "string",
      "external_id_additive": "string",
      "id": 1,
      "new_value_contract": "string",
      "note": "string",
      "number_of_users": 1,
      "renew_in_days": 1,
      "type_additive": "string",
      "value_additive": "string",
      "value_contract": "string",
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
| `client_contract_id` | number |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `date_final` | string |  |
| `date_initial` | string |  |
| `date_sale` | string |  |
| `description` | string |  |
| `external_id_additive` | string |  |
| `id` | number |  |
| `new_value_contract` | string |  |
| `note` | string |  |
| `number_of_users` | number |  |
| `renew_in_days` | number |  |
| `type_additive` | string |  |
| `value_additive` | string |  |
| `value_contract` | string |  |
| `value_per_user` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/contract_additives` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract-additive.md) for the provider-specific parameters and requirements.

