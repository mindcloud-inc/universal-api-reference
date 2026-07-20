# Reepay: Add Payment Method

Adds a payment method in Reepay.

```
POST https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "ct_f96004cae4308473c92bea0638b5b688"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "ct_f96004cae4308473c92bea0638b5b688"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | object | no |  |
| `customer_handle` | string | no |  |
| `reference` | string | no |  |
| `source` | string | yes | The payment method source, for example a one-time card token like ct_f96004cae4308473c92bea0638b5b688. Example: `ct_f96004cae4308473c92bea0638b5b688`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "failed": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "offline_mandate": {
        "offline_agreement_handle": "string",
        "offline_agreement_name": "Ava Chen"
      },
      "payment_type": "string",
      "reference": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `customer` | string |  |
| `failed` | date |  |
| `id` | string |  |
| `offline_mandate.offline_agreement_handle` | string |  |
| `offline_mandate.offline_agreement_name` | string |  |
| `payment_type` | string |  |
| `reference` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `POST /v1/payment_method` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-payment-method.md) for the provider-specific parameters and requirements.

