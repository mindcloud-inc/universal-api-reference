# Tiliter: Create Product Sample

Creates a product sample in the Tiliter Recognition API.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-product-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-product-sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "collectorEmail": "ava@example.com",
  "deviceId": "string",
  "backgroundType": "string",
  "weightGrams": 1,
  "images[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-product-sample', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "collectorEmail": "ava@example.com",
    "deviceId": "string",
    "backgroundType": "string",
    "weightGrams": 1,
    "images[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes |  |
| `collectorEmail` | string | yes |  |
| `deviceId` | string | yes |  |
| `backgroundType` | string | yes |  |
| `weightGrams` | number | yes |  |
| `images[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productId": "string",
      "sampleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productId` | string |  |
| `sampleId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `POST /products/:product_id/samples` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-sample.md) for the provider-specific parameters and requirements.

