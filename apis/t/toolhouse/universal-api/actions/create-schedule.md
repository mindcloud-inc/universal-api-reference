# Toolhouse: Create Schedule



```
POST https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cadence": "string",
  "chatId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cadence": "string",
    "chatId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bundle` | string | no | Optional Toolhouse bundle name. |
| `cadence` | string | yes | The cron cadence for the autonomous run. |
| `callbackUrl` | string | no | Optional webhook URL to receive schedule callbacks. |
| `chatId` | string | yes | The Toolhouse chat ID to schedule. |
| `toolhouseId` | string | no | Optional Toolhouse workspace identifier. |
| `vars` | object | no | Variables passed to scheduled runs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "archived": true,
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
| `archived` | boolean |  |
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

Through the native Toolhouse API, this operation is `POST /schedules` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

