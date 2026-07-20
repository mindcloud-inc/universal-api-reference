# Nozbe Personal: Create Reminder

Creates a new reminder in Nozbe Personal.

```
POST https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "L2TZ05o6wV41fjMe",
  "remindAt": "1767225600000",
  "isRelative": "false",
  "isAllDay": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "L2TZ05o6wV41fjMe",
    "remindAt": "1767225600000",
    "isRelative": "false",
    "isAllDay": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Reminder task ID. Example: `L2TZ05o6wV41fjMe`. |
| `remindAt` | number | yes | Reminder timestamp in milliseconds. Example: `1767225600000`. |
| `isRelative` | boolean | yes | Whether the reminder is relative. Default: `false`. Example: `false`. |
| `isAllDay` | boolean | yes | Whether the reminder lasts all day. Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isAllDay": true,
      "isRelative": true,
      "remindAt": "2026-05-07T12:00:00.000Z",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `isRelative` | boolean |  |
| `remindAt` | date |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `POST /reminders` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reminder.md) for the provider-specific parameters and requirements.

