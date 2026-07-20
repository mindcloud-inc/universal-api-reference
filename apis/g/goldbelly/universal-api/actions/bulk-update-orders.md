# Goldbelly: Bulk Update Orders



```
PUT https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ],
  "orders[].customerReferenceNumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}],
    "orders[].customerReferenceNumber": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | yes | Orders to update. Each item must include a customer reference number and may include merchant status or tracking number. |
| `orders[].customerReferenceNumber` | number | yes | Customer reference number for the order to update. |
| `orders[].merchantStatus` | string | no | Merchant status to set for the order. |
| `orders[].trackingNumber` | string | no | Tracking number to set for the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Goldbelly API, this operation is `POST orders/bulk_update` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-orders.md) for the provider-specific parameters and requirements.

