# Metronome: Get Customer Billing Provider Configurations

Retrieves customer billing provider configurations from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-customer-billing-provider-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-customer-billing-provider-configurations?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-customer-billing-provider-configurations?${params}`, {
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
| `customerId` | string | yes | The customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "string",
      "billing_provider": "string",
      "customer_id": "string",
      "delivery_method": "string",
      "delivery_method_id": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string |  |
| `billing_provider` | string |  |
| `customer_id` | string |  |
| `delivery_method` | string |  |
| `delivery_method_id` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/getCustomerBillingProviderConfigurations` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-billing-provider-configurations.md) for the provider-specific parameters and requirements.

