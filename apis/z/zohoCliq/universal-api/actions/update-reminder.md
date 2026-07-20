# Zoho Cliq: Update Reminder

Updates an existing reminder in Zoho Cliq.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/update-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/update-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reminderId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/update-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reminderId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reminderId` | string | yes | The ID of the reminder to update. |
| `content` | string | yes | The updated reminder content. |
| `time` | number | no | The updated reminder trigger time in milliseconds. |

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

Through the native Zoho Cliq API, this operation is `PUT /reminders/:reminderId` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reminder.md) for the provider-specific parameters and requirements.

