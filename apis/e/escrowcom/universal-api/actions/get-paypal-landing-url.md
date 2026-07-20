# Escrow.com: Get PayPal Landing URL

Retrieves a PayPal landing URL from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-paypal-landing-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-paypal-landing-url?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-paypal-landing-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | number | yes | The Escrow.com transaction ID. |
| `returnUrl` | string | no | Redirect URL used after the customer is redirected to the Escrow PayPal success page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `redirectType` | string | no | Whether the redirect happens automatically or manually via CTA click. |
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
| `landingPage` | string | PayPal landing page URL when PayPal is available for the transaction. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/:transaction_id/payment_methods/paypal` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paypal-landing-url.md) for the provider-specific parameters and requirements.

