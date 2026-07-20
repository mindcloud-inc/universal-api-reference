# PayTabs: Create Recurring Payment



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-recurring-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-recurring-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-recurring-payment', {
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
      "merchantId": 1,
      "paymentResult": {},
      "profileId": 1,
      "trace": "string",
      "tranRef": "string",
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
| `merchantId` | number |  |
| `paymentResult` | object |  |
| `profileId` | number |  |
| `trace` | string |  |
| `tranRef` | string |  |
| `tranType` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/request` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recurring-payment.md) for the provider-specific parameters and requirements.

