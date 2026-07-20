# CustomerX: Delete Customer By External ID

Deletes an existing customer from CustomerX by external ID.

```
DELETE https://connect.mindcloud.co/v1/universal/customerX/latest/actions/delete-customer-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/delete-customer-by-external-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/delete-customer-by-external-id?${params}`, {
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
      "group": "string",
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
| `group` | string |  |
| `id` | number |  |
| `ie_rg` | string |  |
| `number` | string |  |
| `state` | string |  |
| `street` | string |  |
| `trading_name` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `DELETE /api/v1/clients` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-by-external-id.md) for the provider-specific parameters and requirements.

