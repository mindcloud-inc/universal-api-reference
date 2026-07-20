# ChargeDesk: List Subscription Cancellations

Retrieves subscription cancellations from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-subscription-cancellations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-subscription-cancellations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-subscription-cancellations?${params}`, {
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
      "action": "string",
      "customer_id": "string",
      "email": "ava@example.com",
      "ip": "string",
      "method": "string",
      "occurred": 1,
      "reason": "string",
      "subscription_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `customer_id` | string |  |
| `email` | string |  |
| `ip` | string |  |
| `method` | string |  |
| `occurred` | number |  |
| `reason` | string |  |
| `subscription_id` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /log/cancellations` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscription-cancellations.md) for the provider-specific parameters and requirements.

