# Zoho Cliq: Set Self Reminder

Creates a self reminder in Zoho Cliq.

```
POST https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/set-self-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/set-self-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/set-self-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The reminder content. |
| `time` | number | no | The reminder trigger time in milliseconds. |

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

Through the native Zoho Cliq API, this operation is `POST /reminders` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-self-reminder.md) for the provider-specific parameters and requirements.

