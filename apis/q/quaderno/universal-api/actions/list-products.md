# Quaderno: List Products

Retrieves product records from Quaderno.

```
GET https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Filter products by product name or code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": 1,
      "currency": "string",
      "description": "string",
      "id": 1,
      "kind": "string",
      "name": "Ava Chen",
      "productType": "string",
      "stock": "string",
      "taxBasedOn": "string",
      "taxClass": "string",
      "taxType": "string",
      "unitCost": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | number |  |
| `kind` | string |  |
| `name` | string |  |
| `productType` | string |  |
| `stock` | string |  |
| `taxBasedOn` | string |  |
| `taxClass` | string |  |
| `taxType` | string |  |
| `unitCost` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Quaderno API, this operation is `GET /items` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

