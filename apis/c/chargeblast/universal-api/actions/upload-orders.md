# Chargeblast: Upload Orders

Uploads orders to Chargeblast.

```
POST https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeblast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-orders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | yes | The list of orders to upload to Chargeblast. Each order object should follow the documented OrderUploadBodyOrder contract; live runtime in this tenant also required `status` and `last4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | The result message returned by Chargeblast after the order upload. |

## Native endpoint

Through the native Chargeblast API, this operation is `POST /api/v2/orders/upload` (base URL `https://api.chargeblast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-orders.md) for the provider-specific parameters and requirements.

