# Launch27: Exchange FSPay Payment Account

Exchanges an FSPay payment account in Launch27.

```
PUT https://connect.mindcloud.co/v1/universal/launch27/latest/actions/exchange-fspay-payment-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/exchange-fspay-payment-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hosted_payment_account_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launch27/latest/actions/exchange-fspay-payment-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hosted_payment_account_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hosted_payment_account_id` | string | yes | Hosted payment account ID returned by FullSteam hosted payments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fspay_payment_method_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fspay_payment_method_id` | string | Stored FullSteam payment method ID returned after exchanging a hosted payment account ID. |

## Native endpoint

Through the native Launch27 API, this operation is `POST fspay/token/exchange` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/exchange-fspay-payment-account.md) for the provider-specific parameters and requirements.

