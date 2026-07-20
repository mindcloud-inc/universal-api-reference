# ChargeDesk: Retrieve Subscription

Retrieves a subscription from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-subscription?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-subscription?${params}`, {
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
| `subscriptionId` | string | yes | Subscription ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "amount_formatted": "string",
      "company": "string",
      "currency": "string",
      "current_period_end": "string",
      "current_period_start": "string",
      "customer_id": "string",
      "first_seen": 1,
      "gateway_url": "https://example.com",
      "interval": "string",
      "interval_count": "string",
      "manage_url": "https://example.com",
      "methods_active": [
        "string"
      ],
      "methods_supported": [
        "string"
      ],
      "object": "string",
      "product_id": "string",
      "quantity": "string",
      "setup_amount": "string",
      "status": "string",
      "status_text": "string",
      "subscription_id": "string",
      "trial_period_days": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amount_formatted` | string |  |
| `company` | string |  |
| `currency` | string |  |
| `current_period_end` | string |  |
| `current_period_start` | string |  |
| `customer_id` | string |  |
| `first_seen` | number |  |
| `gateway_url` | string |  |
| `interval` | string |  |
| `interval_count` | string |  |
| `manage_url` | string |  |
| `methods_active` | array<string> |  |
| `methods_supported` | array<string> |  |
| `object` | string |  |
| `product_id` | string |  |
| `quantity` | string |  |
| `setup_amount` | string |  |
| `status` | string |  |
| `status_text` | string |  |
| `subscription_id` | string |  |
| `trial_period_days` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /subscriptions/:SUBSCRIPTION_ID` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscription.md) for the provider-specific parameters and requirements.

