# Metronome: Update Customer Configuration

Updates a customer configuration in Metronome.

```
PUT https://connect.mindcloud.co/v1/universal/metronome/latest/actions/update-customer-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/update-customer-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metronome/latest/actions/update-customer-configuration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The customer ID. |
| `leaveStripeInvoicesInDraft` | boolean | no | Whether to leave Stripe invoices in draft. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Metronome API returns.

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/customers/:customer_id/updateConfig` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-configuration.md) for the provider-specific parameters and requirements.

