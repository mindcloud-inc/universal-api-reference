# Fatture in Cloud: Create Product

Creates a new product in Fatture in Cloud.

```
POST https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | The ID of the company. |
| `data` | object | yes | The product payload inside the provider data envelope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "code": "string",
      "defaultVat": {
        "description": "string",
        "id": 1,
        "isDisabled": true,
        "notes": "string",
        "value": 1
      },
      "description": "string",
      "grossPrice": 1,
      "id": 1,
      "inStock": true,
      "measure": "string",
      "name": "Ava Chen",
      "netCost": 1,
      "netPrice": 1,
      "useGrossPrice": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `code` | string |  |
| `defaultVat.description` | string |  |
| `defaultVat.id` | number |  |
| `defaultVat.isDisabled` | boolean |  |
| `defaultVat.notes` | string |  |
| `defaultVat.value` | number |  |
| `description` | string |  |
| `grossPrice` | number |  |
| `id` | number |  |
| `inStock` | boolean |  |
| `measure` | string |  |
| `name` | string |  |
| `netCost` | number |  |
| `netPrice` | number |  |
| `useGrossPrice` | boolean |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `POST /c/:company_id/products` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

