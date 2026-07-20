# ChargeDesk: List Webhook Notifications

Retrieves webhook notifications from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-webhook-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-webhook-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-webhook-notifications?${params}`, {
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
      "description": "string",
      "name": "Ava Chen",
      "notification": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `name` | string |  |
| `notification` | string |  |
| `object` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /webhooks/notifications` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-notifications.md) for the provider-specific parameters and requirements.

