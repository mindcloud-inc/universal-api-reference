# CustomerX: List Contracts

Retrieves a list of contracts from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contracts?${params}`, {
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
      "auto_renovation": true,
      "cancellation_date": "string",
      "cancellation_reason": "string",
      "client_id": 1,
      "contract_plan_id": "string",
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
      "renew_in_days": "string",
      "start_date": "string",
      "status": "string"
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
| `contract_plan_id` | string |  |
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
| `renew_in_days` | string |  |
| `start_date` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/contracts` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

