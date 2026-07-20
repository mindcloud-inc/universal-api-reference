# CustomerX: Get Contract Additive

Retrieves contract additive details from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/get-contract-additive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/get-contract-additive?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/get-contract-additive?${params}`, {
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
      "type_additive": "string",
      "updated_at": "string",
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
| `type_additive` | string |  |
| `updated_at` | string |  |
| `value_additive` | string |  |
| `value_contract` | string |  |
| `value_per_user` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/contract_additives/[:id]` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contract-additive.md) for the provider-specific parameters and requirements.

