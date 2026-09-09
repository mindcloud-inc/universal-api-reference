# Walmart: Refund Order Lines

Issue refunds for return orders.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/refund-order-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/refund-order-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "returnOrderId": "string",
  "customerOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/refund-order-lines', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "returnOrderId": "string",
    "customerOrderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refundLines[]` | array<object> | no | List of return order lines to refund. |
| `refundLines[].quantity.measurementValue` | number | no | Numeric value for the quantity in the specified unit of measure. |
| `refundLines[].returnOrderLineNumber` | number | no | Line number within the return order. Required when the return order contains multiple lines. If the return order contains a single line and this field is not sent, that line is selected automatically. Omitting a required line number results in a data error. |
| `returnOrderId` | string | yes | Return order identifier also known as RMA number. |
| `refundLines[].quantity` | object | no | Quantity to refund on this return line. |
| `refundLines[].quantity.unitOfMeasure` | list<string> | no | Unit of measure for the quantity. Examples include `EACH` or `EA`. |
| `customerOrderId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isDynamicSandbox` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerOrderId": "string",
      "refundLines": [
        {
          "quantity": {
            "measurementValue": 1,
            "unitOfMeasure": "string"
          },
          "returnOrderLineNumber": 1
        }
      ],
      "returnOrderId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerOrderId` | string |  |
| `refundLines[].quantity.measurementValue` | number |  |
| `refundLines[].quantity.unitOfMeasure` | string |  |
| `refundLines[].returnOrderLineNumber` | number |  |
| `returnOrderId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/returns/:returnOrderId/refund` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-order-lines.md) for the provider-specific parameters and requirements.

