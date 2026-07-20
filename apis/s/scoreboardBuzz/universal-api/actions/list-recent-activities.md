# Scoreboard Buzz: List Recent Activities

Retrieves recent activities from Scoreboard Buzz.

```
GET https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-recent-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-recent-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-recent-activities?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "memo": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "quantity": 1,
      "trackable_id": 1,
      "trackable_name": "Ava Chen",
      "user_email": "ava@example.com",
      "user_id": 1,
      "user_name": "Ava Chen",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `id` | number | Activity ID. |
| `memo` | string | Optional memo saved on the activity. |
| `modified` | date | Last modification timestamp. |
| `quantity` | number | Quantity scored for the activity. |
| `trackable_id` | number | Trackable ID scored by the activity. |
| `trackable_name` | string | Trackable name scored by the activity. |
| `user_email` | string | Email address of the user tied to the activity. |
| `user_id` | number | User ID tied to the activity. |
| `user_name` | string | Display name of the user tied to the activity. |
| `value` | number | Value amount scored for the activity. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `GET /activities` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-activities.md) for the provider-specific parameters and requirements.

