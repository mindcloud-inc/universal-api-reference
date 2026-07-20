# Reepay: Get Payment Method

Retrieves a payment method from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-payment-method?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-payment-method?${params}`, {
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
| `id` | string | yes | Payment method identifier from Reepay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "customer": "string",
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
| `id` | string |  |
| `offline_mandate.offline_agreement_handle` | string |  |
| `offline_mandate.offline_agreement_name` | string |  |
| `payment_type` | string |  |
| `reference` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/payment_method/:id` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-method.md) for the provider-specific parameters and requirements.

