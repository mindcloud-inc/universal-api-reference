# Tiliter: Update Store Stock

Updates store stock in the Tiliter Recognition API.

```
PUT https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-store-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-store-stock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storeId": "string",
  "stockStates[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-store-stock', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storeId": "string",
    "stockStates[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeId` | string | yes |  |
| `stockStates[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invalidProductIds": [
        "string"
      ],
      "productStockStates": [
        {
          "productId": "string",
          "stockState": "string"
        }
      ],
      "updatedProductIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invalidProductIds` | array |  |
| `productStockStates` | array<object> |  |
| `productStockStates[].productId` | string |  |
| `productStockStates[].stockState` | string |  |
| `updatedProductIds` | array<string> |  |
| `updatedProductIds[]` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `PUT /stores/:store_id/stock` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-store-stock.md) for the provider-specific parameters and requirements.

