# Global Payments WebPay: Create Link

Creates a payment link in Global Payments WebPay.

```
POST https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/create-link', {
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
      "account_name": "Ava Chen",
      "app_email": "ava@example.com",
      "id": "string",
      "reference": "string",
      "status": "string",
      "type": "string",
      "url": "https://example.com",
      "usage_mode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_name` | string |  |
| `app_email` | string |  |
| `id` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `type` | string |  |
| `url` | string |  |
| `usage_mode` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /links` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

