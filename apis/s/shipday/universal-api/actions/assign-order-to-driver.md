# Shipday: Assign Order to Driver

Assigns an existing order to a driver in Shipday.

```
PUT https://connect.mindcloud.co/v1/universal/shipday/latest/actions/assign-order-to-driver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/assign-order-to-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "44865172",
  "carrierId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipday/latest/actions/assign-order-to-driver', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "44865172",
    "carrierId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | Shipday order ID used in the request path. Example: `44865172`. |
| `carrierId` | number | yes | Shipday carrier ID used in the request path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider message returned after assignment. |
| `success` | boolean | Whether the order assignment succeeded. |

## Native endpoint

Through the native Shipday API, this operation is `PUT /orders/assign/:orderId/:carrierId` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-order-to-driver.md) for the provider-specific parameters and requirements.

