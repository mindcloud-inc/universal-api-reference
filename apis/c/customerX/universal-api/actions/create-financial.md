# CustomerX: Create Financial

Creates a new financial record in CustomerX.

```
POST https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-financial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-financial" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/create-financial', {
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
      "amount_paid": "string",
      "client": {},
      "client_id": 1,
      "created_at": "string",
      "date_due": "string",
      "date_issue": "string",
      "date_original_due": "string",
      "date_payment": "string",
      "description": "string",
      "discount_value": "string",
      "external_id_financial": "string",
      "id": 1,
      "identifier": "string",
      "status": "string",
      "updated_at": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_paid` | string |  |
| `client` | object |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `date_due` | string |  |
| `date_issue` | string |  |
| `date_original_due` | string |  |
| `date_payment` | string |  |
| `description` | string |  |
| `discount_value` | string |  |
| `external_id_financial` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `status` | string |  |
| `updated_at` | string |  |
| `value` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/financials` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-financial.md) for the provider-specific parameters and requirements.

