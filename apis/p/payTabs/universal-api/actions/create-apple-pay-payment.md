# PayTabs: Create Apple Pay Payment



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-apple-pay-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-apple-pay-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-apple-pay-payment', {
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
      "cartAmount": 1,
      "cartCurrency": "string",
      "cartDescription": "string",
      "cartId": "string",
      "customerDetails": {},
      "merchantId": 1,
      "profileId": 1,
      "redirectUrl": "https://example.com",
      "trace": "string",
      "tranRef": "string",
      "tranTotal": 1,
      "tranType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartAmount` | number |  |
| `cartCurrency` | string |  |
| `cartDescription` | string |  |
| `cartId` | string |  |
| `customerDetails` | object |  |
| `merchantId` | number |  |
| `profileId` | number |  |
| `redirectUrl` | string |  |
| `trace` | string |  |
| `tranRef` | string |  |
| `tranTotal` | number |  |
| `tranType` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/request` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-apple-pay-payment.md) for the provider-specific parameters and requirements.

