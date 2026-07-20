# Starshipit: Search Orders



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/search-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/search-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/search-orders?${params}`, {
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
| `limit` | string | no | Amount of results (default: 50) (maximum: 250) |
| `page` | string | no | Page to show (default: 1) |
| `status` | string | no | Returns a list of orders based on the order status (default: All) |
| `fields` | string | no | In. conjunction with the phrase parameter, which field to search. If "All", it will search 'order number', 'tracking number', 'theirRef' and 'name' |
| `includeChildAccounts` | string | no | If set to true, orders from child accounts will be returned (default: false) |
| `phrase` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {
          "carrierName": "Ava Chen",
          "country": "string",
          "name": "Ava Chen",
          "orderDate": "2026-05-07T12:00:00.000Z",
          "orderId": 1,
          "orderNumber": "string",
          "trackingNumber": "string"
        }
      ],
      "success": true,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> |  |
| `orders[].carrierName` | string |  |
| `orders[].country` | string |  |
| `orders[].name` | string |  |
| `orders[].orderDate` | date |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].trackingNumber` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/search` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-orders.md) for the provider-specific parameters and requirements.

