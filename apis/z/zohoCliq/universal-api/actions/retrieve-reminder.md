# Zoho Cliq: Retrieve Reminder

Retrieves a reminder from Zoho Cliq by ID.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-reminder?connectionId=$CONNECTION_ID&reminderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reminderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-reminder?${params}`, {
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
| `reminderId` | string | yes | The ID of the reminder to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "content": "string",
      "creation_time": 1,
      "creator": {},
      "id": "string",
      "time": 1,
      "timezone": "string",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the reminder is completed. |
| `content` | string | The reminder content. |
| `creation_time` | number | Reminder creation time in milliseconds. |
| `creator` | object | The reminder creator. |
| `id` | string | The reminder identifier. |
| `time` | number | The reminder trigger time in milliseconds. |
| `timezone` | string | The reminder timezone. |
| `users` | array<object> | The reminder assignees. |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /reminders/:reminderId` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-reminder.md) for the provider-specific parameters and requirements.

