# Starshipit: List Suggested Merges



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-suggested-merges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-suggested-merges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-suggested-merges?${params}`, {
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
| `limit` | string | no | (default: 50, min: 1, max: 250) |
| `page` | string | no | default: 1 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {
          "orders": [
            {
              "city": "string",
              "contact": "string",
              "country": "string",
              "orderDate": "2026-05-07T12:00:00.000Z",
              "orderId": 1,
              "orderNumber": "string",
              "postcode": "string",
              "state": "string",
              "street": "string",
              "suburb": "string"
            }
          ],
          "primaryOrderId": 1
        }
      ],
      "success": true,
      "total": 1,
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
| `orders[].orders` | array<object> |  |
| `orders[].orders[].city` | string |  |
| `orders[].orders[].contact` | string |  |
| `orders[].orders[].country` | string |  |
| `orders[].orders[].orderDate` | date |  |
| `orders[].orders[].orderId` | number |  |
| `orders[].orders[].orderNumber` | string |  |
| `orders[].orders[].postcode` | string |  |
| `orders[].orders[].state` | string |  |
| `orders[].orders[].street` | string |  |
| `orders[].orders[].suburb` | string |  |
| `orders[].primaryOrderId` | number |  |
| `success` | boolean |  |
| `total` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/mergeable` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suggested-merges.md) for the provider-specific parameters and requirements.

