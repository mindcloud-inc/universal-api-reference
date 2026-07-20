# ChargeDesk: List Subscriptions

Retrieves subscriptions from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-subscriptions?${params}`, {
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

Through the native ChargeDesk API, this operation is `GET /subscriptions` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

