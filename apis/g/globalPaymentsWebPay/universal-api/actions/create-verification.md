# Global Payments WebPay: Create Verification

Creates a payment method verification in Global Payments WebPay.

```
POST https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-verification', {
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
      "channel": "string",
      "country": "string",
      "currency": "string",
      "id": "string",
      "merchant_id": "string",
      "status": "string",
      "time_created": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `channel` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `merchant_id` | string |  |
| `status` | string |  |
| `time_created` | date |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /verifications` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-verification.md) for the provider-specific parameters and requirements.

