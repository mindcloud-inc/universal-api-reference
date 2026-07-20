# vPlan: Get Time Tracking Entry



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-time-tracking-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-time-tracking-entry?connectionId=$CONNECTION_ID&id=2ff2e433-cb2a-4d9c-b16b-3fbf125e8107" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2ff2e433-cb2a-4d9c-b16b-3fbf125e8107"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-time-tracking-entry?${params}`, {
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
| `id` | string | yes | Time tracking entry identifier. Default: `2ff2e433-cb2a-4d9c-b16b-3fbf125e8107`. |

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

Through the native vPlan API, this operation is `GET /time_tracking/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-tracking-entry.md) for the provider-specific parameters and requirements.

