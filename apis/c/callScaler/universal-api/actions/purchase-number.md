# CallScaler: Purchase Number

Creates a purchased number in CallScaler.

```
POST https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/purchase-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/purchase-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/purchase-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "call_flow_id": "string",
      "call_flow_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "friendly_name": "Ava Chen",
      "group_id": "string",
      "group_name": "Ava Chen",
      "id": "string",
      "phone_number": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_flow_id` | string | Assigned call flow ID. |
| `call_flow_name` | string | Assigned call flow name. |
| `created_at` | date | Tracking number creation timestamp. |
| `friendly_name` | string | Friendly name for the tracking number. |
| `group_id` | string | Assigned number group ID. |
| `group_name` | string | Assigned number group name. |
| `id` | string | Unique tracking number ID. |
| `phone_number` | string | Tracking phone number. |
| `status` | string | Tracking number status. |
| `type` | string | Number type. |

## Native endpoint

Through the native CallScaler API, this operation is `POST /numbers/purchase` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-number.md) for the provider-specific parameters and requirements.

