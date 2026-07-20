# Zoho Cliq: Complete Reminder

Marks a Zoho Cliq reminder as complete.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/complete-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/complete-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reminderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/complete-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reminderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reminderId` | string | yes | The ID of the reminder to mark as complete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Cliq API returns.

## Native endpoint

Through the native Zoho Cliq API, this operation is `PUT /reminders/:reminderId/complete` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-reminder.md) for the provider-specific parameters and requirements.

