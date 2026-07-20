# Metronome: Set Customer Billing Provider Configurations

Updates customer billing provider configurations in Metronome.

```
PUT https://connect.mindcloud.co/v1/universal/metronome/latest/actions/set-customer-billing-provider-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/set-customer-billing-provider-configurations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metronome/latest/actions/set-customer-billing-provider-configurations', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_provider": "string",
      "customer_id": "string",
      "delivery_method_id": "string",
      "id": "string",
      "tax_provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_provider` | string |  |
| `customer_id` | string |  |
| `delivery_method_id` | string |  |
| `id` | string |  |
| `tax_provider` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/setCustomerBillingProviderConfigurations` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-customer-billing-provider-configurations.md) for the provider-specific parameters and requirements.

