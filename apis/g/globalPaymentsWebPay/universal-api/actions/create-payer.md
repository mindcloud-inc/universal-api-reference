# Global Payments WebPay: Create Payer

Creates a payer in Global Payments WebPay.

```
POST https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-payer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-payer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-payer', {
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
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "merchant_id": "string",
      "reference": "string",
      "time_created": "2026-05-07T12:00:00.000Z",
      "time_last_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `merchant_id` | string |  |
| `reference` | string |  |
| `time_created` | date |  |
| `time_last_updated` | date |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /payers` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payer.md) for the provider-specific parameters and requirements.

