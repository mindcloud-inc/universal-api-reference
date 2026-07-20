# RO App: Get Order



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-order?${params}`, {
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
| `orderId` | number | yes | Order ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_campaign_id": 1,
      "asset_id": 1,
      "assignee_id": 1,
      "branch_id": 1,
      "client_id": 1,
      "custom_fields": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "engineer_notes": "string",
      "estimated_price": "string",
      "malfunction": "string",
      "manager_id": 1,
      "manager_notes": "string",
      "order_type_id": 1,
      "payer_id": 1,
      "resource_id": 1,
      "resume": "string",
      "scheduled_for": "2026-05-07T12:00:00.000Z",
      "scheduled_to": "2026-05-07T12:00:00.000Z",
      "urgent": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_campaign_id` | number |  |
| `asset_id` | number |  |
| `assignee_id` | number |  |
| `branch_id` | number |  |
| `client_id` | number |  |
| `custom_fields` | string |  |
| `due_date` | date |  |
| `engineer_notes` | string |  |
| `estimated_price` | string |  |
| `malfunction` | string |  |
| `manager_id` | number |  |
| `manager_notes` | string |  |
| `order_type_id` | number |  |
| `payer_id` | number |  |
| `resource_id` | number |  |
| `resume` | string |  |
| `scheduled_for` | date |  |
| `scheduled_to` | date |  |
| `urgent` | boolean |  |

## Native endpoint

Through the native RO App API, this operation is `GET /orders/:order_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

