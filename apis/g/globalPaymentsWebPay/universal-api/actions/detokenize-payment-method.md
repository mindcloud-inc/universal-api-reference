# Global Payments WebPay: Detokenize Payment Method

Retrieves detokenized payment method details from Global Payments WebPay.

```
GET https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/detokenize-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/detokenize-payment-method?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/detokenize-payment-method?${params}`, {
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
| `id` | string | yes | Global Payments payment method ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card": {
        "brand": "string",
        "number": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "reference": "string",
      "status": "string",
      "time_created": "2026-05-07T12:00:00.000Z",
      "usage_mode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card.brand` | string |  |
| `card.number` | string |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `time_created` | date |  |
| `usage_mode` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /payment-methods/{id}/detokenize` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detokenize-payment-method.md) for the provider-specific parameters and requirements.

