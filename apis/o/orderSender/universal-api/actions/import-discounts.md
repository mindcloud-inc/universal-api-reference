# Order Sender: Import Discounts

Imports discount records into Order Sender.

```
POST https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/import-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/import-discounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/import-discounts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Import result message. |
| `result` | string | Import result status. |

## Native endpoint

Through the native Order Sender API, this operation is `POST /op/import/res/sconti` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-discounts.md) for the provider-specific parameters and requirements.

