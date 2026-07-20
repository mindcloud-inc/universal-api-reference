# Razorpay: Get Payment Card Details

Retrieves card details for a payment from Razorpay.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment-card-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment-card-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment-card-details?${params}`, {
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
| `id` | string | yes | Unique identifier of the payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emi": true,
      "entity": "string",
      "id": "string",
      "issuer": "string",
      "last4": "string",
      "name": "Ava Chen",
      "network": "string",
      "subType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emi` | boolean |  |
| `entity` | string |  |
| `id` | string |  |
| `issuer` | string |  |
| `last4` | string |  |
| `name` | string |  |
| `network` | string |  |
| `subType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/payments/:id/card` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-card-details.md) for the provider-specific parameters and requirements.

