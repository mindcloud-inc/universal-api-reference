# ReadyCloud Suite: List Organizations

Retrieves organizations from ReadyCloud Suite.

```
GET https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReadyCloud Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/list-organizations?${params}`, {
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
      "action_alert_custom_domain_enabled": true,
      "action_alert_send_from_alias": "string",
      "app_seat_licenses": [
        {}
      ],
      "avatar": "string",
      "billing_status": "string",
      "cached_orders_views": true,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "equipment_returns_enabled": true,
      "fees_paid_by": "string",
      "member_websocket_channel_id": "string",
      "name": "Ava Chen",
      "payment_plan": {},
      "subscriptions": {},
      "trial_expires_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_slots": 1,
      "wallet_auto_refill_amount": 1,
      "wallet_auto_refill_limit": 1,
      "wallet_charges_allowed": true,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_alert_custom_domain_enabled` | boolean |  |
| `action_alert_send_from_alias` | string |  |
| `app_seat_licenses` | array<object> |  |
| `avatar` | string |  |
| `billing_status` | string |  |
| `cached_orders_views` | boolean |  |
| `deleted_at` | date |  |
| `equipment_returns_enabled` | boolean |  |
| `fees_paid_by` | string |  |
| `member_websocket_channel_id` | string |  |
| `name` | string |  |
| `payment_plan` | object |  |
| `subscriptions` | object |  |
| `trial_expires_at` | date |  |
| `url` | string |  |
| `user_slots` | number |  |
| `wallet_auto_refill_amount` | number |  |
| `wallet_auto_refill_limit` | number |  |
| `wallet_charges_allowed` | boolean |  |
| `website` | string |  |

## Native endpoint

Through the native ReadyCloud Suite API, this operation is `GET /api/v2/orgs/` (base URL `https://www.readycloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

