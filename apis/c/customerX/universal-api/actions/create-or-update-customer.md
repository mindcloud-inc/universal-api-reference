# CustomerX: Create Or Update Customer

Creates or updates a customer in CustomerX.

```
PUT https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-or-update-customer', {
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
      "cancellation_date": "string",
      "cep": "string",
      "city": "string",
      "cnpj_cpf": "string",
      "company_name": "Ava Chen",
      "complement": "string",
      "contract_status": "string",
      "country": "string",
      "date_register": "string",
      "district": "string",
      "email": "ava@example.com",
      "external_id_client": "string",
      "id": 1,
      "ie_rg": "string",
      "number": "string",
      "state": "string",
      "street": "string",
      "trading_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancellation_date` | string |  |
| `cep` | string |  |
| `city` | string |  |
| `cnpj_cpf` | string |  |
| `company_name` | string |  |
| `complement` | string |  |
| `contract_status` | string |  |
| `country` | string |  |
| `date_register` | string |  |
| `district` | string |  |
| `email` | string |  |
| `external_id_client` | string |  |
| `id` | number |  |
| `ie_rg` | string |  |
| `number` | string |  |
| `state` | string |  |
| `street` | string |  |
| `trading_name` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/clients/create_or_update` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

