# Toolhouse: Update Schedule



```
PUT https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/update-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/update-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cadence": "string",
  "scheduleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/update-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cadence": "string",
    "scheduleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | no | Whether the schedule should remain active. |
| `bundle` | string | no | Optional Toolhouse bundle name. |
| `cadence` | string | yes | The cron cadence for the autonomous run. |
| `callbackUrl` | string | no | Optional webhook URL to receive schedule callbacks. |
| `chatId` | string | no | Optional Toolhouse chat ID to re-target the schedule. |
| `scheduleId` | string | yes | The Toolhouse schedule ID. |
| `toolhouseId` | string | no | Optional Toolhouse workspace identifier. |
| `vars` | object | no | Variables passed to scheduled runs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "bundle": "string",
      "cadence": "string",
      "callback_url": "https://example.com",
      "chat_archived": true,
      "chat_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "last_ran_at": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "toolhouse_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vars": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `bundle` | string |  |
| `cadence` | string |  |
| `callback_url` | string |  |
| `chat_archived` | boolean |  |
| `chat_id` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `last_ran_at` | date |  |
| `title` | string |  |
| `toolhouse_id` | string |  |
| `updated_at` | date |  |
| `vars` | object |  |

## Native endpoint

Through the native Toolhouse API, this operation is `PUT /schedules/:schedule_id` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-schedule.md) for the provider-specific parameters and requirements.

