# Escrow.com: Select Payment Method

Selects a transaction payment method in Escrow.com.

```
POST https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/select-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/select-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": 1,
  "paymentMethodName": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/select-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": 1,
    "paymentMethodName": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | number | yes | The Escrow.com transaction ID. |
| `paymentMethodName` | string | yes | Payment method name. Documented values include credit_card, paypal, wire_transfer, and poli. One of: `0`, `1`, `2`, `3`. |
| `wireReference` | string | no | Wire reference number when selecting wire transfer. |
| `returnUrl` | string | no | Return URL used by PayPal or credit card payment flows. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asCustomer` | string | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "landingPage": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `landingPage` | string | Hosted payment landing page URL when Escrow.com returns one for the selected method. |

## Native endpoint

Through the native Escrow.com API, this operation is `POST /transaction/:transaction_id/payment_methods/:payment_method_name` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/select-payment-method.md) for the provider-specific parameters and requirements.

