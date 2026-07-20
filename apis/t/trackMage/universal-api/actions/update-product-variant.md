# TrackMage: Update Product Variant

Updates an existing product variant in TrackMage.

```
PUT https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-product-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-product-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-product-variant', {
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
| `id` | string | yes | Resource identifier |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | no | The URL of product variant image in the ecommerce store. |
| `price` | string | no | The price of product variant in the store currency. Default value is **0** |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalSourceIntegration": "string",
      "externalSourceSyncId": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "price": "string",
      "product": "string",
      "sku": "string",
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalSourceIntegration` | string |  |
| `externalSourceSyncId` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `price` | string |  |
| `product` | string |  |
| `sku` | string |  |
| `team` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `PUT /product_variants/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-variant.md) for the provider-specific parameters and requirements.

