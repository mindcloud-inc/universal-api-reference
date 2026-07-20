# Printify: List Orders

Retrieves orders from a Printify shop.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-orders?connectionId=$CONNECTION_ID&shopId=27141936" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shopId": "27141936"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-orders?${params}`, {
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
| `limit` | number | no | Maximum number of orders to return. |
| `page` | number | no | Result page to fetch. |
| `shopId` | number | yes | Printify shop id. Default: `27141936`. |
| `sku` | string | no | Filter orders by line item SKU. |
| `status` | string | no | Filter orders by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "createdAt": "string",
          "id": "string",
          "shippingMethod": 1,
          "status": "string",
          "totalPrice": 1
        }
      ],
      "perPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].createdAt` | string |  |
| `data[].id` | string |  |
| `data[].shippingMethod` | number |  |
| `data[].status` | string |  |
| `data[].totalPrice` | number |  |
| `perPage` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Printify API, this operation is `GET /shops/:shop_id/orders.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

