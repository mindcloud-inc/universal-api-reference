# WeSupply: Lookup Order By External Order ID

Retrieves an order from WeSupply by external order ID.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/lookup-order-by-external-order-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/lookup-order-by-external-order-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/lookup-order-by-external-order-id?${params}`, {
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
| `orderExternalOrderId` | string | no | The external order ID to look up in WeSupply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerEmail": "ava@example.com",
      "OrderAmountTotal": 1,
      "OrderExternalOrderID": "string",
      "OrderID": "string",
      "OrderStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerEmail` | string |  |
| `OrderAmountTotal` | number |  |
| `OrderExternalOrderID` | string |  |
| `OrderID` | string |  |
| `OrderStatus` | string |  |

## Native endpoint

Through the native WeSupply API, this operation is `GET /orders/lookup` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-order-by-external-order-id.md) for the provider-specific parameters and requirements.

