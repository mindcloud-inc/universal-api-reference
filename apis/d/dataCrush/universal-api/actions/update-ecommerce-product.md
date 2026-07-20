# DataCrush: Update Ecommerce Product

Updates an ecommerce product in DataCrush.

```
PUT https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/update-ecommerce-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/update-ecommerce-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products_json": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/update-ecommerce-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products_json": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products_json` | string | yes | JSON array of product objects matching the provider schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /ecommerce/v1/product/add` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ecommerce-product.md) for the provider-specific parameters and requirements.

