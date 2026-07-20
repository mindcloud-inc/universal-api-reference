# ConnectPay: Authorize Currency Exchange Payment

Authorizes a currency exchange payment in ConnectPay.

```
PUT https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/authorize-currency-exchange-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConnectPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/authorize-currency-exchange-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/authorize-currency-exchange-payment', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentOrderNo` | string | no | Unique payment order number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConnectPay API returns.

## Native endpoint

Through the native ConnectPay API, this operation is `POST /ob/currencyexchangepayments/:paymentOrderNo/authorisations/nosca` (base URL `https://api-stage.connectpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize-currency-exchange-payment.md) for the provider-specific parameters and requirements.

