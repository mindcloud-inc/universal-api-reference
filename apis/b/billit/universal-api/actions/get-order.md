# Billit: Get Order

Retrieves a Billit order by ID.

```
GET https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-order?connectionId=$CONNECTION_ID&orderID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-order?${params}`, {
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
| `orderID` | number | yes | Billit OrderID returned when the invoice or order was created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Customer": {},
      "IsSent": true,
      "OrderID": 1,
      "OrderLines": [
        {}
      ],
      "OrderNumber": "string",
      "OrderStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Customer` | object | Customer party linked to the order. |
| `IsSent` | boolean | Whether the Billit order is marked as sent/exported. |
| `OrderID` | number | Billit order identifier. |
| `OrderLines` | array<object> | Order lines on the Billit order. |
| `OrderNumber` | string | Human-readable Billit order number. |
| `OrderStatus` | string | Current Billit order status. |

## Native endpoint

Through the native Billit API, this operation is `GET /v1/orders/:orderID` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

