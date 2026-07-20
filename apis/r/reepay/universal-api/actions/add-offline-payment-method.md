# Reepay: Add Offline Payment Method

Adds an offline payment method in Reepay.

```
POST https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-offline-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-offline-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offline_agreement_handle": "codex-rtv-1775066629-offline"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-offline-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offline_agreement_handle": "codex-rtv-1775066629-offline"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer_handle` | string | no |  |
| `offline_agreement_handle` | string | yes | The unique offline agreement handle per account, for example offline-cash-dkk-1. Example: `codex-rtv-1775066629-offline`. |
| `reference` | string | no |  |

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

Through the native Reepay API, this operation is `POST /v1/payment_method/offline` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-offline-payment-method.md) for the provider-specific parameters and requirements.

