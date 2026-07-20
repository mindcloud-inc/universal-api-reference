# Global Payments WebPay: Create Sale Or Refund Transaction

Creates a sale or refund transaction in Global Payments WebPay.

```
POST https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-sale-or-refund-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-sale-or-refund-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-sale-or-refund-transaction', {
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
      "account_id": "string",
      "amount": "string",
      "channel": "string",
      "currency": "string",
      "id": "string",
      "merchant_id": "string",
      "status": "string",
      "time_created": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `amount` | string |  |
| `channel` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `merchant_id` | string |  |
| `status` | string |  |
| `time_created` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /transactions` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sale-or-refund-transaction.md) for the provider-specific parameters and requirements.

