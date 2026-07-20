# CustomerX: List Customers

Retrieves a list of customers from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customers?${params}`, {
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
      "client_group_id": "string",
      "client_segment_id": 1,
      "client_service_id": 1,
      "cnpj_cpf": "string",
      "company_name": "Ava Chen",
      "complement": "string",
      "contract_status": "string",
      "country": "string",
      "created_at": "string",
      "custom_attributes": [
        {}
      ],
      "date_register": "string",
      "district": "string",
      "document_type": "string",
      "email": "ava@example.com",
      "external_id_client": "string",
      "facebook": "string",
      "group": "string",
      "id": 1,
      "ie_rg": "string",
      "instagram": "string",
      "journey_products": [
        {}
      ],
      "linkedin": "https://example.com",
      "number": "string",
      "only_journey_by_contract": true,
      "parent_client": {},
      "phones": [
        {}
      ],
      "portfolio": {},
      "segment": {},
      "service": {},
      "site": "string",
      "state": "string",
      "street": "string",
      "tags": [
        {}
      ],
      "trading_name": "Ava Chen",
      "twitter": "string",
      "updated_at": "string",
      "youtube": "string"
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
| `client_group_id` | string |  |
| `client_segment_id` | number |  |
| `client_service_id` | number |  |
| `cnpj_cpf` | string |  |
| `company_name` | string |  |
| `complement` | string |  |
| `contract_status` | string |  |
| `country` | string |  |
| `created_at` | string |  |
| `custom_attributes` | array<object> |  |
| `date_register` | string |  |
| `district` | string |  |
| `document_type` | string |  |
| `email` | string |  |
| `external_id_client` | string |  |
| `facebook` | string |  |
| `group` | string |  |
| `id` | number |  |
| `ie_rg` | string |  |
| `instagram` | string |  |
| `journey_products` | array<object> |  |
| `linkedin` | string |  |
| `number` | string |  |
| `only_journey_by_contract` | boolean |  |
| `parent_client` | object |  |
| `phones` | array<object> |  |
| `portfolio` | object |  |
| `segment` | object |  |
| `service` | object |  |
| `site` | string |  |
| `state` | string |  |
| `street` | string |  |
| `tags` | array<object> |  |
| `trading_name` | string |  |
| `twitter` | string |  |
| `updated_at` | string |  |
| `youtube` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/clients` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

