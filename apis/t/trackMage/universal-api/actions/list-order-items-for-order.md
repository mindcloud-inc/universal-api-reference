# TrackMage: List Order Items For Order

Retrieves order items for an order in TrackMage.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-order-items-for-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-order-items-for-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-order-items-for-order?${params}`, {
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
| `id` | string | yes | Order identifier |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | The collection page number Default: `1`. |
| `itemsPerPage` | number | no | The number of items per page Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "externalProductId": "string",
      "externalProductLink": "https://example.com",
      "externalSourceIntegration": "string",
      "externalSourceSyncId": "string",
      "fulfilledQty": 1,
      "id": "string",
      "imageUrl": "https://example.com",
      "order": "string",
      "price": "string",
      "product": "string",
      "productName": "Ava Chen",
      "productOptions": {},
      "productSku": "string",
      "productVariant": "string",
      "qty": 1,
      "refundedQty": 1,
      "rowTotal": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `externalProductId` | string |  |
| `externalProductLink` | string |  |
| `externalSourceIntegration` | string |  |
| `externalSourceSyncId` | string |  |
| `fulfilledQty` | number |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `order` | string |  |
| `price` | string |  |
| `product` | string |  |
| `productName` | string |  |
| `productOptions` | object |  |
| `productSku` | string |  |
| `productVariant` | string |  |
| `qty` | number |  |
| `refundedQty` | number |  |
| `rowTotal` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `GET /orders/{id}/items` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-items-for-order.md) for the provider-specific parameters and requirements.

