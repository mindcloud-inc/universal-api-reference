# Tiliter: Update Product Mapping

Updates a product mapping in the Tiliter Recognition API.

```
PUT https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-product-mapping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-product-mapping" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "archetypeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-product-mapping', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "archetypeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes |  |
| `archetypeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archetypeId": "string",
      "productId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archetypeId` | string |  |
| `productId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `PUT /product_mappings/` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-mapping.md) for the provider-specific parameters and requirements.

