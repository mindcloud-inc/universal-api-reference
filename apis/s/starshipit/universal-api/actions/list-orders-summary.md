# Starshipit: List Orders Summary



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-summary?${params}`, {
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
| `orderStatus` | string | no | order status to show order summary of. |
| `sort` | string | no | Order field to sort by. |
| `sortDirection` | string | no | sort direction. |
| `filter` | string | no | Filter the orders returned in the order summary by various filters. This parameter is specified in the following format: Multiple filters can be specified, please seperate these by comma ','. See the Filters section below for accepted filter values. |
| `page` | string | no | page number. |
| `pageSize` | string | no | number of results to return (default: 500, maximum: 500) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderCounts": {
        "archivedCount": 1,
        "archivedShippedCount": 1,
        "archivedUnshippedCount": 1,
        "printedCount": 1,
        "returnCount": 1,
        "shippedCount": 1,
        "unprintedCount": 1,
        "unprintedInvalidaddressCount": 1
      },
      "orders": [
        {
          "carrier": "string",
          "contactName": "Ava Chen",
          "country": "string",
          "integrationId": 1,
          "items": "string",
          "manifestNumber": 1,
          "manifestSent": true,
          "orderDate": "2026-05-07T12:00:00.000Z",
          "orderId": 1,
          "orderNumber": "string",
          "orderStatus": 1,
          "orderType": "string",
          "platform": "string",
          "product": "string",
          "quantity": "string",
          "shippedDate": "2026-05-07T12:00:00.000Z",
          "skus": "string",
          "soh": "string",
          "state": "string",
          "validAddress": true,
          "weight": 1,
          "weightUnit": "string",
          "writebackStatus": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderCounts` | object |  |
| `orderCounts.archivedCount` | number |  |
| `orderCounts.archivedShippedCount` | number |  |
| `orderCounts.archivedUnshippedCount` | number |  |
| `orderCounts.printedCount` | number |  |
| `orderCounts.returnCount` | number |  |
| `orderCounts.shippedCount` | number |  |
| `orderCounts.unprintedCount` | number |  |
| `orderCounts.unprintedInvalidaddressCount` | number |  |
| `orders` | array<object> |  |
| `orders[].carrier` | string |  |
| `orders[].contactName` | string |  |
| `orders[].country` | string |  |
| `orders[].integrationId` | number |  |
| `orders[].items` | string |  |
| `orders[].manifestNumber` | number |  |
| `orders[].manifestSent` | boolean |  |
| `orders[].orderDate` | date |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].orderStatus` | number |  |
| `orders[].orderType` | string |  |
| `orders[].platform` | string |  |
| `orders[].product` | string |  |
| `orders[].quantity` | string |  |
| `orders[].shippedDate` | date |  |
| `orders[].skus` | string |  |
| `orders[].soh` | string |  |
| `orders[].state` | string |  |
| `orders[].validAddress` | boolean |  |
| `orders[].weight` | number |  |
| `orders[].weightUnit` | string |  |
| `orders[].writebackStatus` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/summary` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-summary.md) for the provider-specific parameters and requirements.

