# Tiliter: Create Or Update Products Batch

Creates or updates products in Tiliter in a batch.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-or-update-products-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-or-update-products-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-or-update-products-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "productId": "string",
          "result": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].productId` | string |  |
| `data[].result` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `POST /products/batch` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-products-batch.md) for the provider-specific parameters and requirements.

