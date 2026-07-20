# vPlan: Create Time Tracking Entry



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-time-tracking-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-time-tracking-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-time-tracking-entry', {
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
      "activity_id": "string",
      "card_id": "string",
      "created_at": "string",
      "duration": 1,
      "end": "string",
      "external_failed": true,
      "external_note": "string",
      "external_ref": "string",
      "id": "string",
      "locked": true,
      "note": "string",
      "running": true,
      "start": "string",
      "status": "string",
      "synchronized_at": "string",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity_id` | string | Activity identifier. |
| `card_id` | string | Card identifier. |
| `created_at` | string | Creation timestamp. |
| `duration` | number | Tracked duration. |
| `end` | string | End timestamp. |
| `external_failed` | boolean | Whether external sync failed. |
| `external_note` | string | External note. |
| `external_ref` | string | External reference. |
| `id` | string | Time tracking identifier. |
| `locked` | boolean | Whether the entry is locked. |
| `note` | string | Internal note. |
| `running` | boolean | Whether the timer is running. |
| `start` | string | Start timestamp. |
| `status` | string | Time tracking status. |
| `synchronized_at` | string | Last synchronization timestamp. |
| `updated_at` | string | Last update timestamp. |
| `user_id` | string | User identifier. |

## Native endpoint

Through the native vPlan API, this operation is `POST /time_tracking` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-tracking-entry.md) for the provider-specific parameters and requirements.

