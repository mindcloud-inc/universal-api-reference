# Payrexx: Get Payment Method

Retrieves a payment method from Payrexx.

```
GET https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/get-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/get-payment-method?connectionId=$CONNECTION_ID&paymentMethod=twint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentMethod": "twint"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/get-payment-method?${params}`, {
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
| `paymentMethod` | string | yes | ID of the payment method (e.g. twint or mastercard). Example: `twint`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `GET PaymentMethod/:paymentMethod/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-method.md) for the provider-specific parameters and requirements.

