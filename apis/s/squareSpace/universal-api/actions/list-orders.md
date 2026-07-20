# SquareSpace: List Orders

Retrieves orders from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-orders?${params}`, {
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
| `customerId` | string | no | Filter orders by customer profile ID. |
| `fulfillmentStatus` | list<string> | no | Filter orders by fulfillment status. One of: `CANCELED`, `FULFILLED`, `PENDING`. |
| `modifiedAfter` | date | no | Return orders modified after this datetime. |
| `modifiedBefore` | date | no | Return orders modified before this datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination metadata including next cursor. |
| `result` | array<object> | Order rows returned by Retrieve All Orders. |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /1.0/commerce/orders` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

