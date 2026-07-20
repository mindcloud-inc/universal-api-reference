# Prerender.io: List Billing Is Payment Info Valid

Retrieves payment info validation from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-is-payment-info-valid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-is-payment-info-valid?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-is-payment-info-valid?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "hasPaymentMethod": true,
      "isAddressValid": true,
      "isCreditCardValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasPaymentMethod` | boolean |  |
| `isAddressValid` | boolean |  |
| `isCreditCardValid` | boolean |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/billing/is-payment-info-valid` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-billing-is-payment-info-valid.md) for the provider-specific parameters and requirements.

