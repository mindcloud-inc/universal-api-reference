# Kiwify: Update Affiliate

Updates an existing affiliate in Kiwify.

```
PUT https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/update-affiliate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/update-affiliate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/update-affiliate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `commission` | number | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate_id": "string",
      "commission": 1,
      "company_cnpj": "string",
      "company_name": "Ava Chen",
      "created_at": "string",
      "director_cpf": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "product": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate_id` | string |  |
| `commission` | number |  |
| `company_cnpj` | string |  |
| `company_name` | string |  |
| `created_at` | string |  |
| `director_cpf` | string |  |
| `email` | string |  |
| `name` | string |  |
| `product` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Kiwify API, this operation is `PUT /v1/affiliates/:id` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-affiliate.md) for the provider-specific parameters and requirements.

