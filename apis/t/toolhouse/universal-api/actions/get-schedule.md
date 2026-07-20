# Toolhouse: Get Schedule



```
GET https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/get-schedule?connectionId=$CONNECTION_ID&scheduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/get-schedule?${params}`, {
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
| `scheduleId` | string | yes | The Toolhouse schedule ID. |

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

Through the native Toolhouse API, this operation is `GET /schedules/:schedule_id` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

